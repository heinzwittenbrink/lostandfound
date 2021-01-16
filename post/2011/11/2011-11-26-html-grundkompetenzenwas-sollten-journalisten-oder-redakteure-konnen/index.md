---
title: "HTML-Grundkompetenzen—Was sollten Journalisten und Redakteure können?"
date: "2011-11-26"
categories: 
  - "allgemein"
tags: 
  - "lernmittel"
  - "studium"
  - "web-literacy"
---

Vor einer Woche habe ich [versucht, die Kompetenzen zu beschreiben](http://heinz.typepad.com/lostandfound/2011/11/mit-newsfeeds-umgehen-k%C3%B6nneneine-basiskompetenz.html "Mit Newsfeeds umgehen könneneine Basiskompetenz - Lost and Found"), die man braucht, um Newsfeeds in einem journalistischen oder redaktionellen Workflow zu verwenden. Wir sind mit diesem Programm in der Lehrveranstaltung nicht fertig geworden. Da wir gestern im selben Kurs mit dem Thema HTML begonnen haben, versuche ich hier nach demselben Schema zu beschreiben, welche Kompetenzen man im Editieren von Text für das Web benötigt.

Ob und wie sich das umsetzen lässt, kann ich in der Wiener und in der Grazer Einführung für die Journalismus-Erstsemester ausprobieren. Das ist für mich auch deshalb interessant, weil die Programme der Lehrveranstaltungen und die didaktischen Methoden verschieden sind.

Was sollte man können, um einen Text zu schreiben, der im Web publiziert wird—z.B. in einem Blog, auf einer News-Site oder in einem Wiki? Die folgende Liste ist sicher nicht endgültig:

- Sowohl einen grafischen ([WYSIWYG](http://de.wikipedia.org/wiki/WYSIWYG "WYSIWYG – Wikipedia")\-) Editor wie ein Editorfenster für Quelltext benutzen und zwischen beidem problemlos wechseln,
    
- wenn es nötig ist, das [Markup](http://de.wikipedia.org/wiki/Markup "Auszeichnungssprache – Wikipedia") so editieren, dass keine syntaktischen Fehler entstehen,
    
- Links sowohl im grafischen wie im Quelltext-Editor eingeben und auf Korrektheit überprüfen,
    
- Medien, also Photos, Videos und Audios einbetten,
    
- das Aussehen von Elementen verändern, also z.B. die Textgröße für eine Creditline anpassen,
    
- HTML-Elemente verwenden, die z.B. für die Kommentare in einem Blog erlaubt sind,
    
- Textformate zum vereinfachten Schreiben von HTML wie [Markdown](http://markdown.de/syntax/ "markdown.de | Markdown Syntax-Dokumentation") (hier als Beispiel; eine Alternative ist [Textile](http://www.textism.com/tools/textile/ "Textism: Tools: Textile")) oder ein [Wiki Markup](http://en.wikipedia.org/wiki/Wiki_markup "Wiki markup - Wikipedia, the free encyclopedia") benutzen,
    
- Links und HTML-Quelltext aus einem Dokument und in ein HTML-Dokument kopieren,
    
- ein Dokument als HTML-Dokument abspeichern und exportieren und Teile daraus verwenden,
    
- Fehler korrigieren, die durch das Kopieren von Texten aus Word und anderen Textverarbeitungen entstehen,
    
- ein Dokument [validieren](http://validator.w3.org/ "The W3C Markup Validation Service"),
    
- Teile eines Dokuments im Quelltext z.B. auf Suchmaschinengerechtigkeit überprüfen,
    
- HTML-Templates anpassen.
    

Diese Fähigkeiten sind nicht für alle ein Must, die im Web schreiben wollen. Man kommt lange ohne sie aus, sehr lange ohne die drei letzten. Man ist dann allerdings oft schon bei banalen Problemen auf Hilfe angewiesen—z.B. wenn man, wie oben erwähnt, etwas aus MS Word in ein HTML-Dokument kopiert. Außerdem ist man davon abhängig, dass das Content Management System, das man verwendet, alle gewünschten Formate (z.B. für Bildunterschriften) zur Verfügung stellt. Man verliert Tempo, weil man z.B. nicht schnell Links mit einem Browser-Addon wie [Make Link](https://addons.mozilla.org/en-US/firefox/addon/make-link/ "Make Link :: Add-ons for Firefox") oder [Create Link](https://chrome.google.com/webstore/detail/gcmghdmnkfdbncmnmlkkglmnnhagajbm "Chrome Web Store - Create Link") kopieren, und weil man Tools wie Markdown nicht nutzen kann. Und schließlich: Man versteht nicht, was man tut, man kann nicht mitreden, wenn es um die Weiterentwicklung eines Webauftritts geht, und man liefert sich Experten oder Leuten aus, die sich als solche ausgeben.

### Ein Beispiel: Mein HTML-Workflow beim Bloggen

Es gibt sicher nicht den typischen Workflow bei der Textproduktion. Aber wahrscheinlich gilt für alle, dass mehrere Tools und Prozesse zusammenspielen. Dieses Zusammenspiel ist wohl am wichtigsten, wenn man Kompetenzen vermitteln will.

Bei meinem eigenen Workflow—wenn ich blogge, aber auch wenn ich andere Texte schreibe—sind meist Links der Anfang und HTML das Endergebnis. Zum Schreiben benutze ich einen Texteditor, der Markdown unterstützt, dazu später. Um die Links in den Text zu bekommen, verwende ich eine Browsererweiterung, wenn ich an einem Computer arbeite: Make Link im Firefox, Create Link im Chrome. Mit beiden erhalte ich die Links schon im Markdown-Format. Dabei habe ich die Extensions so konfiguriert, dass ich sie auch für Quellenangaben bei Zitaten im für mich richtigen Format (in eckigem Klammern) bekomme. Auf dem iPad kopiere ich die URLs aus dem Safari. Mit dem [TextExpander](http://itunes.apple.com/us/app/textexpander/id326180690?mt=8 "App Store - TextExpander") und der [IOS-Markdown-Gruppe von Snippets](http://brettterpstra.com/markdown-snippets-for-textexpander-on-ios/ "Markdown snippets for TextExpander touch - Brett Terpstra") setze ich sie dann formatiert in mein Dokument. Meinen Text schreibe ich meist um die Links herum, wobei ich inzwischen meist versuche, von einer Outline mit den Hauptaussagen aus nach unten zu arbeiten. Dabei nehme ich als Editor inzwischen meist den [iA Writer](http://www.iawriter.com/ "iA Writer"), manchmal auch den [Markdown Mode](http://jblevins.org/projects/markdown-mode/ "Emacs Markdown Mode") des Emacs. Wenn der Text fertig ist, ergänze ich noch fehlende Links. Wenn ich Videos einbette, kopiere ich den entsprechenden HTML-Code in mein Markdown-Dokument. Dann kopiere ich das Ganze in das Editor-Fenster meines Blogging-Dienstes Typepad. Typepad unterstützt Markdown, der Quelltext bleibt also in diesem Format. (Für andere Systeme konvertiere ich auf der Kommandozeile den Markdown-Text in ein HTML-Fragment.) Im Typepad-Editor füge ich Bilder ein, die ich auf den Server laden muss. Dann schaue ich mir eine Vorschau an, redigiere bzw. korrigiere den Text und publiziere ihn. Wenn ich Credit Lines oder ähnliches brauche, schreibe ich sie in HTML und benutze das Attribut `style` zum Formatieren.

Ich schreibe also nur ganz wenig echtes HTML, obwohl ich keinen grafischen Editor benutze. Ich kann so schnell arbeiten und kontrollieren, was ich produziere. Ich könnte nicht so arbeiten, wenn ich nicht wüsste, wie HTML funktioniert.

Das alles klingt vielleicht etwas geekig. Dieser Workflow verlangt aber viel weniger technisches Wissen als das Arbeiten mit Office-Programmen, und er produziert portable Texte in einem einfachen, standardisierten Format.

### Was sollte ich über HTML wissen, wenn ich im Web publiziere?

Wie bei allen Literacies gibt es hier kein ganz oder gar nicht, nur ein mehr oder weniger. Wenn man nicht wenigstens Basiskenntnisse der HTML-Syntax besitzt und eine Text-Datei nicht von einem Word-Dokument unterscheiden kann, riskiert man unerwünschte Ergebnisse, z.B. nicht vernarbte Word-Formatierungen. Ich versuche hier das Basiswissen aufzulisten (im Sinne von »präpositionalem Wissen«, nicht von Beherrschung von Tools), das ein professioneller Kommunikator heute besitze sollte.

Was muss man wissen, um praktisch zu können, was ich oben beschrieben habe:

- Man muss wissen, was eine reine Textdatei ist, wie sie sich von anderen Formaten für Text unterscheidet, und auch, wie sie kodiert, also in Bytes übersetzt wird.
    
- Man muss wissen, was ein Texteditor im Unterschied zu einem WYSIWYG-Editor ist.
    
- Man muss wissen, wie HTML-Markup funktioniert und was die wichtigsten syntaktischen Elemente sind.
    
- Man muss die Grundstruktur eines HTML-Dokuments kennen.
    
- Man sollte ein Grundwissen über die verschiedenen Versionen von HTML haben, vor allem über die Unterschiede zwischen dem HTML aus der Zeit der Browser Wars, XHTML und HTML5.
    
- Man sollte wissen, was es heißt, ein Dokument zu validieren, und wie man das macht.
    
- Man sollte wissen, was Markup generell ist, was XML ist und wozu es dient.
    
- Man muss den Unterschied von Inhalt und Präsentation und die Funktionen von HTML, CSS und JavaScript kennen.
    
- Man muss die Grundregeln von Mardkdown- und/oder Wiki-Markup kennen.
    
- Man muss Tools zum Verwandeln von Markdown in HTML kennen bzw. wissen, was sie tun.
    
- Man muss wissen, wo man die HTML-, CSS-, Markdown- und Wiki-Syntax nachschlagen kann.
    

Diese Liste ist erweiterbar. Man muss gleich einige Punkte an sie anhängen, wenn man verstehen will, wie ein CMS funktioniert, was heute mit HTML5 möglich ist oder was JavaScript ist. Aber das gehört, so wichtig es ist, nicht mehr zur Basiskompetenz des Editierens von HTML.
