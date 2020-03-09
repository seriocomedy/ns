---
title: LiteTube Redesign
date: 2018-10-13
---
<img src="litetube.png" alt="LiteTube Screenshot">
<p>
I have redesigned <a href="https://yt.dorper.me">LiteTube</a> to be more modern, responsive and usable. I replaced the custom CSS with UIKit 3 and have also cut down on the number of client-side dependencies. VideoJS has been completely removed because it kept breaking.
Search is now displayed as a list of cards and video descriptions now support links. Channels and playlists are not implemented yet because neither youtube-dl or youtube-node support fast channel and playlist listing (youtube-dl takes over 25 seconds to list the videos from a small channel).
The source code has also been moved back to <a href="https://launchpad.net/dorptube">Launchpad</a>.
