---
title: CSS Grid Polyfill
date: 2018-02-15
---
<table id="layout">
    <tbody>
        <tr>
            <td colspan="2" id="header"><h1>Dank Site</h1></td>
        </tr>
        <tr>
            <td id="aside" width="15%">
                <ul>
                    <li><a href="#">Home</a></li>
                    <li><a href="#">Memes</a></li>
                    <li><a href="#">About</a></li>
                </ul>
            </td>
            <td id="main">
                <h1>Home</h1>
                <p>Ok, this site is epic.</p>
            </td>
        </tr>
        <tr>
            <td colspan="2" id="footer"><p>&copy; 2018 Carver Harrison - Original Character Do Not Steal</p></td>
        </tr>
    </tbody>
</table>grid-template-areas:
    'header header header header header header header header'
    'aside main main main main main main main'
    'footer footer footer footer footer footer footer footer';<h1>CSS Grid Polyfill</h1>
<div>Recently, a new feature in CSS called <em>CSS Grids</em> has been released. However many browsers don't support this new feature. For this reason I have created a Polyfill for CSS Grids that uses <strong>no Javascript</strong>.</div>
<div>Take a site using this CSS:</div>
%highlightfile '/www/werc/sites/dorper.me/news/2018/02/15/css-grid-polyfill/ex.css' css
<div>It can be rewritten using this HTML</div>
%highlightfile '/www/werc/sites/dorper.me/news/2018/02/15/css-grid-polyfill/example.html' html
<div>This works on
<strong>all</strong>
browsers.</div>
<div><em>NOTE: The author does not condone the use of <code>&lt;table&gt;</code> for layout.</em></div></div>
