---
title: "PubsubHubbub: Newsfeeds in Echtzeit"
date: "2009-08-09"
categories: 
  - "allgemein"
tags: 
  - "syndication"
  - "tools"
---

Für die Medien ist der wichtigste Trend im Web der Übergang zum _Realtime-Web_. [Twitter](http://twitter.com/ "Twitter / Home") ist das spektakulärste Beispiel für einen Service, über den man Informationen in Echtzeit austauschen kann (es geht um Austausch und um beliebige Quellen, nicht um isolierte Dienste wie etwa Börsenticker.) [Google Wave](http://wave.google.com/ "Google Wave Preview"), im Gegensatz zu Twitter hochkomplex, soll Echtzeit-Kollaboration erlauben, um etwa gemeinsam und dezentral Medien zu produzieren und aktuell zu halten. (Google Wave basiert nicht auf den gängigen Web-Techniken, sondern auf dem [XMPP-Protokoll](http://de.wikipedia.org/wiki/Extensible_Messaging_and_Presence_Protocol "Extensible Messaging and Presence Protocol – Wikipedia"); Anil Dash z.B. [zweifelt deshalb daran](http://dashes.com/anil/2009/08/what-works-the-web-way-vs-the-wave-way.html "What Works: The Web Way vs. The Wave Way - Anil Dash"), dass es sich im Web, das inkrementelle Veränderungen bevorzugt, durchsetzen kann.)

PubsubHubbub erlaubt Twitter-artige Echtzeit-Updates, aber unabhängig von einem zentralen Server wie bei Twitter.

> Es ist nett zu sehen, dass wenigstens ein paar Leute bei Google die Möglichkeit sehen, ein Twitter-artiges Benachrichtigungssystem im _Small Pieces Loosely Joined-Stil_ zu entwickeln,

schreibt [Dave Winer](http://www.scripting.com/stories/2009/07/10/googlesPubsubhubbub.html "It's nice to see that at least a few people at Google see the possibility of assembling a Twitter-like notification system with the Small Pieces, Loosely Joined approach.") \[via [hackr](http://hackr.de/ "hackr")\].

Es handelt sich um eine Erweiterung zu Atom-Newsfeeds (die Ausdehnung auf RSS 2.0 ist geplant). 'Hubbub-befähigte Feeds enthalten ein Link zu einem _Hub_, an den sie Aktualisierungen in Echtzeit melden, und der seinerseits Clients, die ihn abonniert haben, sofort über die Änderung informiert. Der Client (z.B. ein Online-Newsreader) muss die Informationen also nicht mehr _pollen_ (=zu einer Zeit _x_ abrufen), sondern die Informationen werden an ihn _gepusht_. Für die Benutzer bedeutet das: So wie sie jetzt via Twitter Statusmeldungen erhalten, können sie bald beliebige Informationen in Echtzeit abonnieren. Voraussetzung ist nur ein Newsfeed, der der mit 'Hubbub arbeitet.

Der Google Reader verwendet jetzt 'Hubbub [bei den Empfehlungen (Shared Items)](http://googlereader.blogspot.com/2009/08/pubsubhubbub-support-for-reader-shared.html "Official Google Reader Blog: PubSubHubbub support for Reader shared items"). Friendfeed, ebenfalls 'Hubbub-enabled, wird damit fast augenblicklich über neue Shared Items informiert und stellt sie sofort dar. Wie das aussieht, zeigt dieses Demo-Video:

Auch [Feedburner](http://feedburner.google.com "Feedburner"), Googles Service zum Erzeugen und Vermarkten von RSS-Feeds, unterstützt dieses Abo-Verfahren; dazu gibt es ein neues Feature namens _PingShot_, das man für seinen Feed nur auswählen muss. Aktualisierungen werden dann, wie bei den Shared Items im Reader, an einen Hub-Server von Google geschickt und weiterverteilt. (Ich weiss nicht, ob er mit Googles [Demo-Server](http://pubsubhubbub.appspot.com/ "Hub - PubSubHubbub") für das neue Feed-Subskriptionsverfahren identisch ist.)

PubsubHubbub ist eine offene Technologie, die nicht Google gehört. Google unterstützt sie aber intensiv. Google gehörte auch zu den frühesten Implementierern des [Atom](http://de.wikipedia.org/wiki/Atom_(Format) "Atom (Format) – Wikipedia")\-Formats, auf denen 'Hubbub basiert. Mehr Informationen gibt es auf der [Projekt-Site](http://code.google.com/p/pubsubhubbub/ "pubsubhubbub - Project Hosting on Google Code") und im ersten [Entwurf der Spezifikation](http://pubsubhubbub.googlecode.com/svn/trunk/pubsubhubbub-core-0.1.html "Draft: PubSubHubbub Core 0.1 -- Working Draft"). Wie ein PubsubHubbub-Server, also ein _Hub_, arbeitet, zeigt [diese Präsentation](http://docs.google.com/present/view?id=ajd8t6gk4mh2_34dvbpchfs "Updated Pubsubhubbub flow presentation").

Ich werde mich mit 'Hubbub (und dem [Pushbutton Web](http://dashes.com/anil/2009/07/the-pushbutton-web-realtime-becomes-real.html "The Pushbutton Web: Realtime Becomes Real - Anil Dash")) intensiver beschäftigen, dieses Post ist nur ein erster Hinweis. (Auf Deutsch habe ich außer [diesem Post](http://www.fabianpimminger.com/tech/pubsubhubbub/ "PubSubHubbub – Push für Nachrichten-Feeds - Tech - Fabian Pimminger") Fabian Pimmingers nicht viel darüber gefunden.) Das Verfahren wird es vor allem erlauben, zu bestimmten Themen (_Topics_) Echtzeit-Informationen zu erhalten: Wie interessant das für Journalismus und Unternehmenskommunikation ist, liegt auf der Hand.
