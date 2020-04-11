---
title: XtOS
---
<h1 class="page-title">XtOS</h1>
<p class="page-desc">The Xt Operating System</p>

XtOS is an operating system written in C and Assembly.

## Minimum Requirements
- CPU: Intel i386
- RAM: 2MB
- GPU: Any VGA Card
- HDD: 3½ floppy drive or IDE hard disk with at least 300KB free space
- I/O: IBM PC compatible I/O

## Tested Hardware
### HP t5145
This is the system that XtOS is developed on so it should work fine with XtOS.
- CPU: VIA Eden @ 500Mhz
- RAM: 512MB DDR2
- Chipset: VIA VX800
- I/O: VIA VT1211 Super I/O
- GPU: VIAChrome9 HC3
- HDD: 128MB IDE Flash Module
- BootOS: FreeDOS 1.2

## Running XtOS
### In QEMU
1. Download [xtos.img](https://mirror.dorper.me/xtos/xtos.img).
2. Install [QEMU](https://www.qemu.org).
3. Run `qemu-system-i386 -fda xtos.img -m 64M`

### On Real Hardware
1. Download [xtos.img](https://mirror.dorper.me/xtos/xtos.img).
2. Write `xtos.img` to a blank 1.44MB 3½ floppy disk using one of the following tools:
	- Windows: [DiskWrite](http://freeextractor.sourceforge.net/diskwrite/)
	- Linux: `dd`
3. Insert the floppy disk into a computer and boot.

## Design
### Development
XtOS is developed using [NASM](https://nasm.us) and [OpenWatcom](http://www.openwatcom.org) on a HP t5145 running [FreeDOS 1.2](https://freedos.org).
Code is edited using [UW Pico](https://itconnect.uw.edu/connect/web-publishing/shared-hosting/using-piconano/).
Debugging for `LOADER.COM` and `STAGE2.BIN` is provided by the Watcom Debugger. No debugger is available for `KERNEL.386`.

### Boot
#### Stage 0: FreeDOS
XtOS Boots from FreeDOS, a open source clone of DOS.
The FreeDOS kernel is loaded into HIGH memory to leave space for Stage 2.

#### Stage 1: LOADER.COM
`LOADER.COM` is the loader for both `STAGE2.BIN` and `KERNEL.386`.
It uses INT 21h services to read both files into memory. `STAGE2.BIN` is loaded somewhere in the first 64K of memory.
`KERNEL.386` is loaded at `0x30000`. After both files are loaded successfully, `LOADER.COM` jumps to `STAGE2.BIN`.

#### Stage 2: STAGE2.BIN
`STAGE2.BIN` disables interrupts, loads the initial GDT, switches to protected mode, and jumps to `KERNEL.386` in under 100 bytes.

#### Stage 3: KERNEL.386
`KERNEL.386` is the XtOS protected mode kernel. On startup, it loads its own GDT, IDT, and enables interrupts.