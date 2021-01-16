---
title: "Google Gears"
date: "2007-06-03"
tags: 
  - "tools"
---

Wir überlegen am [Studiengang](http://www.fh-joanneum.at/aw/home/Studienangebot/Medien_und_Design/~czf/juk/?lan=de) gerade, ob wir ein neues EDV-Labor mit Desktop-Rechnern einrichten, oder ob wir den Studenten Notebooks sponsorn sollen. Gestern habe ich mich durch Technik-News und Blog-Einträge der vergangenen Woche gewühlt — die wohl wichtigste ist für mich ein weiteres Argument dafür, vom mobilen Arbeiten als dem Normalfall auszugehen und also auch dafür auszubilden: Google hat eine frühe Beta von [Google Gears](http://gears.google.com/) publiziert.

Gears ist ein Browser-Plugin, mit dem man Webanwendungen weiterbenutzen kann, wenn man offline ist. Eine erste Musteranwendung ist der [Google Reader](http://googlereader.blogspot.com/2007/05/oh-sam-i-am-can-i-read-it-on-tram.html). Wenn man Gears installiert, kann man durch Klicken auf einen Button auf die Offline-Version umschalten; dann werden die 2000 neuesten Einträge lokal gespeichert. Ist man wieder online, synchronisiert Gears die loalen Daten und die Daten im Netz. Als Beispiel für Programmierer hat Google auch einen einfachen Notepad entwickelt.

Interessant finde ich nicht so sehr die Möglichkeit, ohne Netzverbindung offline weiterarbeiten zu können. Ich würde die Perspektive drehen: Jede Offline-Tätigkeit kann via Gears und Verwandte einfach online fortgesetzt werden. Jeder Text und jedes Foto bekommt einen URI und ist damit potentiell im Web erreichbar. Auch Arbeitsmaterial usw. Gears ist ein weiterer Schritt zur _Universalisierung des Publizierens_.

Etwas Material für spätere Verwendung:

### Schnittstelle für Entwickler

Gears funktioniert nur bei Anwendungen, die speziell für dieses Plugin entwickelt wurden (Dokumentation im [Developer Guide](http://code.google.com/apis/gears/index.html)). Dazu bietet es drei JavaScript-APIs an, also Schnittstellen für Entwickler. Über diese Schnittstellen werden ein zeitweiliger lokaler Webserver (ein URL-Cache) und eine lokale SQL-Datenbank angesprochen, außerdem ein thread repository für die Abarbeitung der Programmierlogik. Mit Gears kann man nicht nur Anwendungen im Web weiterbenutzen, wenn man gerade keine Internetverbindung hat. Über Gears können auch rechenintensive Teile von Programmen auf einem Webserver an den Client-Rechner delegiert werden. Die Anwendungen werden damit schneller.

### Verbündeter Adobe — Skepsis bei Mozilla

Mit nur wenig Fantasie lässt sich ausmalen, was Google mit Gears anfangen wird: Erste Gears-Kandidaten nach dem Reader dürften Gmail und Google Docs sein. Google hat Gears aber nicht nur für den eigenen Bedarf entwickelt. Es handelt sich um eine Open Source-Anwendung mit einer sehr liberalen Lizenz, jeder Entwickler und jedes Unternehmen kann sie benutzen. Google will die Gears APIs außerdem als Standard vorschlagen. Die Pointe bei dieser Nachricht ist, dass Google mit Adobe bereits ein weiteres Industrie-Schwergewicht für Gears gewonnen hat. Adobe wird bei seiner Rich-Client-Plattform [Apollo](http://labs.adobe.com/wiki/index.php/Apollo) Gears verwenden (dazu [dieser Computerworld-Artikel](http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=9022118&intsrc=news_ts_head)). Auch Microsoft könnte bei [Silverlight](http://www.microsoft.com/silverlight/default01.aspx) auf Gears zurückgreifen, das scheint aber eher eine theoretische Möglichkeit zu sein.

Google-Vertreter haben bei der Ankündigung von Gears auch über Verhandlungen mit der Mozilla-Foundation über Gears-Unterstützung gesprochen; ob die MF eigene Entwicklungen einstellt, um Gears zu übernehmen, [ist aber wenigstens unsicher](http://www.linuxworld.com/news/2007/060107-google-gears-no-slam-dunk-for.html).

### Links

Der beste Artikel zu Gears, den ich gefunden habe: Scott Delap — [Google Gears: Industry Reactions The Day After](http://www.infoq.com/news/2007/06/googlegears)

Weitere Informationen/Einschätzungen zu Gears — eine ziemlich willkürliche Auswahl angesichts der Masse an Artikeln und Blog-Postings:

Gute [kurze Darstellung auf techcrunch](http://www.techcrunch.com/2007/05/30/google-gears-lets-developers-take-apps-offline/); zu den Konsequenzen für die alltägliche Arbeit: [Dumb Little Man —How Google Gears Will Change Your Life](http://www.dumblittleman.com/2007/06/how-google-gears-will-change-your-life.html); [Dare Obasanjo](http://www.25hoursaday.com/weblog/PermaLink.aspx?guid=f61d1dd0-e0f6-48d1-9009-77a5d8a423f0) (Zitat:What matters is that 'it doesn't work offline' is no longer a valid criticism for Google's family of Microsoft office knock offs (i.e. Google Docs & Spreadsheets) or any other AJAX/Flash application that competes with a desktop application...Welcome to the future); [Robert Scoble](http://scobleizer.com/2007/05/30/google-brings-developers-offline-with-gears-new-offline-reader/).
