---
title: "Encoding Fun..."
date: "2005-02-22"
tags: 
  - "i18n-trackbacks"
  - "syndication"
---

Das Trackback, das ich gerade an den [RSS-Blogger](http://www.rss-blogger.de/b2e/blogs/) [geschickt](http://www.rss-blogger.de/b2e/blogs/index.php?title=pladoyer_gegen_rss_v_0_91&more=1&c=1&tb=1&pb=1#feedbacks) habe, ist offenbar in UTF-8, also in der Kodierung dieses Blogs angekommen. Dort produziert es Buchstabensalat. Wie kann man das vermeiden? Gestern hat Sam Ruby auf Jacques Distlers [Internationalization and Trackbacks](http://golem.ph.utexas.edu/~distler/blog/archives/000514.html) hingewiesen ([Sam Ruby: Encoding Fun](http://www.intertwingly.net/blog/2005/02/19/Encoding-Fun)), das genau darstellt, was man tun könnte (und mit Movable Type auch tun kann), damit man ein Trackback in der Kodierung seines Blogs erhält. Ruby selbst hat ein [ein ähnliches Verfahren](http://www.intertwingly.net/blog/2004/06/30/Unicode-Enabled-Trackbacks) für Python beschrieben.

Aber wie kann man bestimmen, in welchem Encoding ein Trackback geschickt wird?
