---
title: How to Change MAC Addresses
---
<p>If you get blocked from a network, one way to get around it is by changing your MAC Address. This tutorial will be Linux specific.</p>
<p>To change your MAC Address, run this as root and replace <code>interface</code> with your network interface:</p>
<pre>sudo ip link set dev &lt;interface&gt; address XX:XX:XX:XX:XX:XX</pre>
<p>You now should be able to reconnect to the network with no issues.</p>