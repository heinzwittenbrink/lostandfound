---
title: "Was ist Hypertext?"
date: "2008-07-23"
categories: 
  - "schreiben-und-hypermedia"
tags: 
  - "html"
  - "hypertext"
---

Wer jemals auf einer Webseite auf ein Link geklickt hat wie [dieses](http://de.wikipedia.org/wiki/Hypertext "Hypertext – Wikipedia"), weiß, wie man mit Hypertext (englische Aussprache [hier](http://www.merriam-webster.com/cgi-bin/audio.pl?hypert03.wav=hypertext "Aussprache von 'hypertext' im Merriam Webster-Wörterbuch")) umgeht. Wie legt man ein solches Link an? Die Erklärung ist vielleicht etwas trocken, aber sie erleichtert es zu verstehen, um was es sich bei Hypertext handelt.

Die meisten Webseiten sind in HTML geschrieben, einem Code zum Verfassen von Hypertext. Bei einem HTML-Dokument wie dem, das ich hier gerade schreibe, stellt der Browser Code wie den folgenden als _Link_ (oder _Hyperlink_) dar:

```
<a href="http://de.wikipedia.org/wiki/Hypertext"
title="Hypertext – Wikipedia">dieses</a>
```

Das Wort `dieses` ist mit zwei _Tags_ — das sind die Zeichenketten in den Spitzklammern, englische Aussprache [hier](http://www.leo.org/dict/audio_en/tag.mp3 "Aussprache von 'tag' im LEO-Wörterbuch") — als Links ausgezeichnet oder markiert. Die hintere Auszeichnung, das _Schlusstag_ `</a>`, sagt nur, dass der markierte Bereich zu Ende ist. Die vordere Auszeichnung, das _Starttag_, hat mehrere Funktionen. Der Buchstabe `a` (eigentlich ein _Elementnamen_), sagt, dass es sich bei dem markierten Textteil `dieses` um ein Link handelt, eine Verknüpfung mit anderen Informationen. Ein Webbrowser gibt ein solches Link in der Regel farbig und unterstrichen wieder; wenn man mit der Maus darüberfährt, verändert sich der Cursor in eine Hand mit ausgestrecktem Zeigefinger. (Das `a` steht für das englische Wort _anchor_, Anker.) Die beiden Zeichenketten `href="http://de.wikipedia.org/wiki/Hypertext"` und `title="Hypertext – Wikipedia"` sind _Attribute_. Der Wert des ersten Attributs — die Zeichenkette `http://de.wikipedia.org/wiki/Hypertext"` — bezeichnet eine bestimmte _Ressource_ im Web; nämlich den Artikel über Hypertext in der deutschsprachigen Wikipedia. Wenn ich im Browser auf das Link klicke, öffnet sich dieser Artikel. Der Wert des zweiten Attributs — `Hypertext – Wikipedia` — sagt mir, um welche Ressource es sich handelt. Wenn ich das Link mit der Maus überfahre, öffnet sich ein ganz kleines Fenster und gibt mit diesen Titel an. Die Buchstabenkette `href`, der Name des ersten Attributs, steht für _hyper reference_, deutsch: _Hyper-Verweis_. Ein Webbrowser, also die Software, mit der ich ein HTML-Dokument lese, ist dazu in der Lage, diesem Verweis zu folgen und sein Ziel darzustellen, im selben oder in einem anderen Browserfenster. Dazu braucht er natürlich sehr viel Infrastruktur, um die es hier jetzt nicht geht.

Ein HTML-Dokument — also ein Text, der in der _Hypertext Markup Language_ geschrieben ist — wird durch Links zu Hypertext. Hypertext ist nicht einfach Text, der mit anderem Text verknüpft ist. Jeder Text bezieht sich auf andere Texte; die _Intertextualität_ ist ein altes Thema in Sprachwissenschaft, Linguistik und Philosophie. Das Besondere an Hypertext ist, dass ich der Verknüpfung sofort folgen kann, dass ich die Verweise nicht nur in meinem Kopf realisiere — eventuell mit Hilfe von Büchern oder anderen Texten, die ich mir besorgt habe. Mit Hypertext habe ich es zu tun, wenn ich — z.B. indem ich auf ein Link klicke — direkt von dem Text, den ich lese, zu einem anderen Text übergehen kann, auf den der erste Text verweist. Aber auch diese Übergangsmöglichkeit reicht eigentlich nicht aus, um Hypertext zu definieren: Zwei Texte die aufeinander verweisen und die nebeneinander vor mir auf dem Tisch liegen, machen noch keinen Hypertext. Zum Hypertext gehört, dass der eine Text die Verbindung zum anderen (das _Link_) in sich enthält. Goethes Werther ist kein Hypertext, weil ich auf ihn verlinke; aber [dieses Link](http://gutenberg.spiegel.de/?id=5&xid=3793&kapitel=1#gb_found "Die Leiden des jungen Werther im Projekt Gutenberg") macht meinen Text hypertextuell.

Hypertext ist Text, der mir als Leser die technische Möglichkeit bietet, die Lektüre sofort durch andere Texte, Textpassagen oder Informationen als die unmittelbar benachbarten fortzusetzen. Dabei verknüpft die Autorin nur bestimmte Teile eines Texts mit bestimmten Zielen. Als Leser kann ich diese Verknüpfungen realisieren, muss es aber nicht. Hypertext ist _interaktiver_ Text; ich kann, über das Lesen hinaus, etwas mit ihm _machen_, Informationen mit ihm ansteuern. Ein Hypertext-Dokument kann ich — selbst wenn es nur ein einziges Link enthält — nicht nur lesen, sondern als _Anwendung_ oder _Programm_ benutzen.

Die Ausdrücke _Anwendung_ und _Programm_ stammen aus der Informatik; Hypertext wird mit Computern (im weitesten Sinn) geschrieben und rezipiert. Das bedeutet aber nicht, dass es sich bei Hypertext um so etwas wie Computertext handelt; Computer werden dazu benutzt, um Hypertexte zu verwirklichen, so wie sie auch dazu benutzt werden, Berechnungen durchzuführen. Hypertexte sind Texte, die die Möglichkeit bieten, mit Informationen zu interagieren, die mit Computern (und Netzwerken) in Echtzeit produziert oder bereitgestellt werden.

Noch zwei Hinweise:

Den Ausdruck _Hypertext_ hat [Ted Nelson](http://xanadu.com.au/ted/ "Ted Nelson Home Page") in der 60er Jahren des letzten Jahrhunderts geprägt. Das Konzept selbst ist älter; oft wird Vannevar Bushs Aufsatz [As We May Think](http://www.theatlantic.com/doc/194507/bush "As We May Think") von 1945 als erste Beschreibung eines Hypertext-Systems genannt. Durchgesetzt hat sich Hypertext durch das World Wide Web, das nichts anderes ist als ein weltweites Hypertext-System auf der Basis des Internet. (Das Internet ist mit dem World Wide Web nicht identisch; Email ist zum Beispiel auch ein Teil des Internet, hat aber mit dem WWW ursprünglich nichts zu tun.) Im World Wide Web wurde bei weitem nicht alles verwirklicht, was Ted Nelson und andere Vordenker des Hypertexts entworfen haben. Umgekehrt bestimmt vor allem die Entwicklung des WWW, was heute Hypertext ist. Zur Zeit wird die [fünfte Version von HTML](http://www.w3.org/html/wg/html5/ "HTML 5") definiert; HTML ist nach wie vor das wichtigste technische Format für Hypertext, aber nicht das einzige.

Formulierungen wie As we may think oder Ted Nelsons Motto [SOMEBODY'S GOT TO DISAGREE](http://ted.hyperland.com/notherview/ "SOMEBODY'S GOT TO DISAGREE") legen es nahe: Hypertext ist eine Sache der Leute, die [Jean-Pol Martin](http://de.wikipedia.org/wiki/Jean-Pol_Martin "Jean-Pol Martin – Wikipedia") _Weltverbesserer_ nennt. So wie der Buchdruck eine Kulturrevolution ausgelöst hat, tut es heute der Hypertext — und dieser Wirkung haben seine Vordenker beabsichtigt. Links unterstützen vernetztes, nichtlineares Denken; sie verbinden nicht nur Texte, sondern auch Menschen. 

https://youtu.be/NLlGopyXT\_g

Das Video _The Machine is Us_ von Michael Wesh beschwört das utopische Potenzial, das der Hypertext noch nicht verloren hat:

\[Erste Version dieses Textes: 23.7.2008. Update, 13.6.2018: Code für das eingebettete Video und diesen Absatz aktualisiert.\]
