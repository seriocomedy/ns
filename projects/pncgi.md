---
title: CGI Perlin Noise
---
<h1 class="page-title">CGI Perlin Noise Generator</h1>
[Interesting Sample](https://x.dorper.me/cgi-bin/pncgi.py?x=100&y=100&o=100&s=333)

I made this perlin noise generator back in 2015. It is not very good and generates to a HTML table instead to an image.
The code is really poorly written and I can't be bothered to fix any more bugs in it.

## Generator Form
<form action="https://x.dorper.me/cgi-bin/pncgi.py" method="GET">
<label for="x">X:</label> <input type="number" name="x" min="0" max="400" value="100"><br>
<label for="y">Y:</label> <input type="number" name="y" min="0" max="400" value="100"><br>
<label for="o">Offset:</label> <input type="number" name="o" min="0" max="400" value="100"><br>
<label for="s">Seed:</label> <input type="text" name="s" size="25"><br>
<input type="submit" value="Generate">
</form>