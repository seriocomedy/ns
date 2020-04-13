---
title: CGI Perlin Noise
---
<h1 class="page-title">CGI Perlin Noise Generator</h1>

I made this perlin noise generator back in 2015. It is not very good and generates to a HTML table instead to an image.
The code is really poorly written.

## Generator Form
<form action="https://x.dorper.me/cgi-bin/pncgi.py" method="GET">
<label for="x">X:</label> <input type="number" min="0" max="400" value="100"><br>
<label for="y">Y:</label> <input type="number" min="0" max="400" value="100"><br>
<label for="o">Offset:</label> <input type="number" min="0" max="400" value="100"><br>
<label for="s">Seed:</label> <input type="text" size="25"><br>
<input type="submit" value="Generate">
</form>