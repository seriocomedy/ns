---
title: Dch
---
<h1 class="page-title">Dch</h1>
<a href="https://c.d0.cx/a?ref=dorper" target="_blank">Visit Dch</a>
<p>
	Dch is a imageboard and comment system. It is written in Python.
</p>

## Features
- File uploading (PNG / JPG)
- Subject lines
- Passwords for post deletion
- Thread tagging which is very useful if you want to use Dch as a comment section.
- Country flags
- [Advanced text formatting](#advanced-formatting)
- <span style="color:#789922">&gt;greentext</span>
- Post Links: <a href="https://c.d0.cx/t/1#1" style="color:#D00">&gt;&gt;1</a><br>
- Capcodes: <span style="color:#FF0000"><b>Carver</b> ★ Admin</span>
- Tripcodes: <span style="color:#117743"><b>Anonymous</b>!bfAJ1WM0</span>
- Options:
	- noflag: hides your country's flag.
	- thread: brings you back to the thread that you were replying to.

## Screenshots
<div class="screenshots">
	{% include lbitem.html src="dch/tform.png" alt="Thread Form" size="300" %}
	{% include lbitem.html src="dch/thread.png" alt="Thread" size="300" %}
</div>

{% include lightbox.html el=".screenshots a" %}

## Embedding Dch
<p>
	Using Dch as the comment system for your site is very simple. Just insert this code and replace <code>PAGE_URL</code> with a unique page id (allowed characters: A-z, 1-9, _).
</p>
<pre>
	<code class="html">
&lt;iframe id="commentsiframe" src="https://c.d0.cx/e/PAGE_URL?noedittag=1" frameborder="0" width="100%" height="500px"&gt;&lt;/iframe&gt;
	</code>
</pre>

## Formatting
### Advanced Formatting
<table>
	<thead>
		<th>Command</th>
		<th>Description</th>
	</thead>
	<tbody>
		<tr><td>@@bold on@@</td><td>Enables bold text.</td></tr>
		<tr><td>@@bold off@@</td><td>Disables bold text.</td></tr>
		<tr><td>@@italic on@@</td><td>Enables italic text.</td></tr>
		<tr><td>@@italic off@@</td><td>Disables italic text.</td></tr>
	</tbody>
</table>

### Example
<table>
	<thead>
		<th>Input</th>
		<th>Output</th>
	</thead>
	<tbody>
		<tr>
			<td>
<pre>
&gt;greentext should be used to quote
See this post:
&gt;&gt;1
This text is normal.
@@bold on@@
This text is bold.
@@italic on@@
This text is both bold and italic.
@@italic off@@
@@bold off@@
</pre>
			</td>
			<td>
				<span style="color:#789922">&gt;greentext should be used to quote</span><br>
				See this post:<br>
				<a href="https://c.d0.cx/t/1#1" style="color:#D00">&gt;&gt;1</a><br>
				This text is normal.<br>
				<b>This text is bold.<br>
				<i>This text is both bold and italic.<br></i></b>
			</td>
		</tr>
	</tbody>
</table>