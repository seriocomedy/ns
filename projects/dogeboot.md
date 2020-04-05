---
title: DogeBoot
---
<h1 class="page-title">DogeBoot</h1>
<a href="https://mirror.dorper.me/dogeboot/dogeboot.asm" target="_blank">Source Code (ASM)</a> &bull; 
<a href="https://mirror.dorper.me/dogeboot/dogeboot.bin" target="_blank">Bootsector (BIN)</a>
<div>
	<a href="{{"/media/img/dogeboot.png"|relative_url}}" target="_blank">
	   <img src="{{"/media/img/dogeboot.png"|relative_url}}" alt="DogeBoot">
	</a>
</div>
<p>
	DogeBoot is a 512-byte real mode bootsector demo featuring <a href="https://en.wikipedia.org/wiki/Doge_(meme)">Doge</a>.
	It renders a stale doge meme on a 40x25 (mode 00h) screen. It is impressive because without compression, it would take 1000 bytes
	to store the meme. However, using a basic compression algorithm, I was able to fit the meme in under 510 bytes.
</p>