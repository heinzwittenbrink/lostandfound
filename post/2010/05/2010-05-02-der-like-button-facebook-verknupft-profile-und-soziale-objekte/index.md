---
title: "Der Like Button: Facebook verknüpft Profile und soziale Objekte"
date: "2010-05-02"
categories: 
  - "allgemein"
tags: 
  - "markup"
  - "social-software"
  - "web-standards"
---

Ich beginne damit, mich mit Facebooks [Like Button](http://developers.facebook.com/docs/reference/plugins/like "Like Button - Facebook Developers") und vor allem mit dem damit verbundenen [Open Graph Protocol](http://developers.facebook.com/docs/opengraph "Open Graph protocol - Facebook Developers") zu beschäftigen. Beide wurden auf der [f8](http://www.facebook.com/f8 "Facebook | f8"), der letzten Facbook-Entwickler-Konferenz, vorgestellt.

Mit dem Like Button kann man bei beliebigen Seiten im Web angeben, dass man sie mag. Dass man sie _geliked_ hat, wird im eigenen Activity Stream bei Facebook angezeigt. Das Open Graph Protocol sorgt darüber hinaus dafür, dass Seiten im Web, die Menschen oder Gegenstände in der realen Welt darstellen, mit dem Profil der Personen verbunden werden, die sie mögen, die also auf den Like Button klicken. Es integriert Informationen über das Objekt und seinem Typ in den _Social Graph_, der alle Facebook-User (oder alle Web-User?) verbindet.

In diesem Blog z.B. findet sich der Like Button rechts; die Informationen über das Blog selbst finden sich im `head` der HTML-Seite, sind also nur im Quelltext sichtbar:

```
<meta property="og:title" content="Lost and Found" />
<meta property="og:type" content="blog" />
<meta property="og:url" content="http://heinz.typepad.com/lostandfound/" />
<meta property="fb:admins" content="536403981" />
```

Wer den Like Button klickt, teilt damit mit, dass er ein _Blog_ mag, dass es _Lost and Found_ heisst und unter dem URI _http://heinz.typepad.com/lostandfound_ erreichbar ist. Der Like Button dient in Verbindung mit Open Graph nicht einfach dazu, Dinge zu teilen oder zu empfehlen, sondern er drückt eine Beziehung aus, und zwar unabhängig von Facebook. Andere Webapplikationen können auf dieselben Metainformationen zurückgreifen.

Eine große Site, die das Open Graph Protocol unterstützt, ist die [Internet Movie Database](http://www.imdb.com/ "The Internet Movie Database (IMDb)"). Wenn ich dort bei einem Film auf den Like Button klicke, findet er sich unter den Lieblingsfilmen in [meinem Profil](http://www.facebook.com/heinzwittenbrink#!/heinzwittenbrink?v=info "Facebook | Heinz Wittenbrink") bei Facebook.

Es ist eine unübersehbare Zahl von Artikeln und Blogposts darüber geschrieben worden, welche Folgen diese im Grunde einfache Technik haben wird. Entscheidend ist dabei, dass Facebook mit bald 500 Millionene Nutzern eine der größten Websites der Welt ist. Das Open Graph Protocol hat damit das Potenzial, das gesamte Web mit Facebook und seinen Nutzern zu verknüpfen—oder besser: die Profile der Facebook-Nutzer mit jeder beliebigen Seite im Web und vor allem mit den auf ihr dargestellten Objekten.

Der für mich interessanteste Aspekt des Open Graph Protocol ist, dass es mit [RDFa](http://en.wikipedia.org/wiki/RDFa "RDFa - Wikipedia, the free encyclopedia") eine _Semantic Web_\-Technologie populär macht. Vielleicht wird es tatsächlich einmal als Durchbruch in Richtung Web 3.0 gefeiert werden. Durch Open Graph werden zum ersten Mal in großem Umfang Informationen aufgrund von semantischen Meta-Daten verknüpft, also etwa der Angabe, dass eine Seite ein Buch, ein Geschäft oder einen Sportler repräsentiert. Ein sehr interessantes Blogpost über die Perspektiven dieser Technologie hat Dare Obasanjo geschrieben: [Facebook’s Open Graph Protocol from a Web Developer’s Perspective](http://25hoursaday.com/weblog/2010/04/24/FacebooksOpenGraphProtocolFromAWebDevelopersPerspective.aspx "Dare Obasanjo aka Carnage4Life - Facebook’s Open Graph Protocol from a Web Developer’s Perspective"). Obasanjo ist ein wichtiger Microsoft-Entwickler; seine Stellungnahme spricht daür, dass Microsoft die neue Facebook-Technologie ebenso unterstützen wird wie voraussichtlich Yahoo! (dazu [Will Yahoo Monkey Around With Open Graph?](http://www.semanticweb.com/news/will_yahoo_monkey_around_with_open_graph_160100.asp#more "Will Yahoo Monkey Around With Open Graph? - Semantic Web")). Obasanjo bezieht sich übrigens ausdrücklich auf den Begriff des _Sozialen Objekts_: Der Like Button drückt Beziehungen zu sozialen Objekten aus (und man könnte erweitern: er schafft auch eine bestimmte Beziehung zu solchen Objekten).

Für meinen Unterricht sehe ich eine Reihe von Konsequenzen der Entwicklungen bei Facebook. Like Button und Open Graph schaffen neue Möglichkeiten für Benutzer-Profile und damit auch für das Reputationsmanagement (dazu sehr gut Klaus Eck: [Gefalle ich Dir? Der Siegeszug des Like-Buttons](http://klauseck.typepad.com/prblogger/2010/04/facebook-internet.html "PR Blogger: Gefalle ich Dir? Der Siegeszug des Like-Buttons")). Sie werden einen großen Einfluss auf die Distribution von Nachrichten haben, vielleicht einen größeren, als die bisherigen Sharing-Technologien, da sie enger mit der Online-Identität der Empfehlenden verbunden sind. Vor allem aber wird für mich deutlich, dass semantische Technologien jetzt den Mainstream erreichen. Sie werden zum Handwerkszeug zukünftger Journalisten und Kommunikatoren gehören, und darauf sind wir noch nicht vorbereitet.
