---
title: Solving the issue of website bloat
date: 2017-12-15 00:00:00 Z
categories:
- programming
description: How minification could improve speeds on your website.
author: Carver Harrison
---

HTML, CSS and Javascript bloat is getting out of hand. Website bloat slows down your site, makes users annoyed and costs money. These are ways that you can remove bloat from your website

## Minification
Javascript and CSS are a major offender when it comes to bloat. The good thing is that this is easy to fix. If you use any Javascript or CSS libraries (jQuery, Bootstrap, AngularJS, etc.), make sure to download the minified version which usually has `min` in the filename.

## Debulk
If you don't have any Javascript code, then you don't need Javascript libraries. Removing any unneeded Javascript libraries from your page will speed up your webpage.

## Customize
If you use a framework like Bootstrap, you are able to select what components you want. Instead of choosing everything, choose only the things you need. For example, if you use bootstrap just for the grid, then only include the grid or better yet, find a more lightweight stylesheet that does the same job better like [Flexbox Grid](http://flexboxgrid.com).

## Leverage the Server
Don't have the client compile templates or retrieve data to put into a table when the server can do that much quicker and without the pain that comes with AJAX. If possible, have the server compile templates and insert components, otherwise, you are using Javascript as a glorified frameset.
