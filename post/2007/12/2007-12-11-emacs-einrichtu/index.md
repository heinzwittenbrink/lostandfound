---
title: "Emacs-Einrichtung unter Leopard: rechte ctrl-Taste, markdown-mode"
date: "2007-12-11"
tags: 
  - "tools"
---

(Dieses Posting wird Lesern, die sich nicht für Themen wie das Max OS X oder Emacs begeistern können, wohl etwas seltsam erscheinen. Ich bitte sie, ein anderes Mal hier vorbeizuschauen. Ich werde gelegentlich wieder vernünftig.)

Mein Arbeitgeber hat mich mit einem neuen MacBook ausgestattet, mit 2 GB RAM und [Leopard](http://www.apple.com/de/macosx/ "Apple - Mac OS X Leopard") als Betriebssystem. Im letzten Jahr habe ich meist auf einem Windows-Notebook gearbeitet, oft auch an einem iMac in meinem Büro, aber ohne die Mac-spezifischen Features zu nutzen. Jetzt muss ich mich fast wieder an den Mac als meine Plattform gewöhnen. Um es mit meinem Sohn David zu sagen: Geil! Coltrane statt James Last...

Mit diesem Rechner möchte ich umgehen können wie mit einem Instrument. Ich möchte das Gerät so konfigurieren und seine Funktionen so gut lernen, dass ich mich darauf konzentrieren kann zu schreiben. Und zu den guten Vorsätzen gehört auch, zu dokumentieren, was ich installiere oder verändere und was ich lerne. Damit fange ich hier an; vielleicht hat irgendeine Leserin ähnliche Probleme, vielleicht erhalte ich ja auch ein paar Tipps.

Die wichtigste Software für mich ist ein Texteditor. Ich schreibe am liebsten mit dem Emacs, auf diesem Gerät in seiner OS X-Spielart [Aquamacs](http://aquamacs.org/ "Aquamacs: Emacs for Mac OS X"). Um das Notebook wirklich wie ein Instrument benutzen zu können, muss ich auch die verschiedenen Kommando- und Funktionstasten blind bedienen können; das beherrsche ich bisher nicht. Eine Schwierigkeit beim Verwenden des Emacs auf einem MacBook: Es gibt rechts keine `ctrl`\-Taste. Viele Emacs-Befehle lassen sich deshalb nicht bequem ausführen. Erst nach einigem Suchen habe ich in [Remapping keys in Mac OS X 10.4](http://desp.night.pl/keys.html) gefunden, wie sich die rechte Apfeltaste (`cmd`) in eine `ctrl`\-Taste verwandeln lässt, ohne zusätzliche Software zu installieren. Das klappt bei Leopard so gut wie bei dem hier beschriebenen System 10.4.

Eine wichtige Ergänzung: Der [markdown-mode](http://jblevins.org/projects/markdown-mode/ "Emacs markdown-mode - Jason Blevins"), der Markdown-Markup farbig unterlegt und Shortcuts für die Eingabe zur Verfügung stellt. Ich benutze [Markdown](http://daringfireball.net/projects/markdown/ "Daring Fireball: Markdown"), um mein Weblog zu schreiben. Auch beim Markdown-Mode bin ich nicht sofort dahinter gekommen, wie man ihn installiert. Den Lisp-Code zur Installation muss man offenbar in die Datei ~/Library/Preferences/Aquamacs Emacs/Preferences.el schreiben statt in das gewohnte ~/.emacs.

(Gäbe es nicht bequemere Editoren als ausgerechnet den Emacs? Ich kann es nicht beurteilen. Ich halte an ihm fest, weil ich ihn wenigstens etwas kenne, weil ich hin und wieder den [nXML mode](http://www.thaiopensource.com/nxml-mode/ "nXML mode") zum Editieren von XML brauche, und weil er unter jedem Betriebssystem funktioniert. Ausserdem mag ich das archaische look-and-feel des Emacs.)

Den nächsten Schritt bewahre ich mir für einen neuen Eintrag auf: Wie schaffe ich es, Aqamacs über das Firefox-Addon [It's All Text!](https://addons.mozilla.org/de/firefox/addon/4125 "It's All Text! :: Firefox Add-ons") als Editor für HTML-Textfelder zu starten. Bisher verhindern das bei mir wohl die zusätzlichen Sicherheitseinstellungen von Leopard.
