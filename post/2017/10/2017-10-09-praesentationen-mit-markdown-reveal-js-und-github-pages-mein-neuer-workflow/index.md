---
title: "Präsentationen mit Markdown, reveal.js und Github Pages: mein neuer Workflow"
date: "2017-10-09"
categories: 
  - "schreiben-und-hypermedia"
tags: 
  - "markdown"
---

Am Samstag habe ich in meiner ersten Lehrveranstaltung für unseren neuen Lehrgang [Technische Dokumentation](https://www.fh-joanneum.at/technische-dokumentation/postgraduate/) die Präsentation [Technische Kommunikation und Content-Strategie](https://heinzwittenbrink.github.io/slides-csandtc/) gezeigt. Ich habe sie via [GitHub Pages](https://pages.github.com/) publiziert.

In Zukunft möchte ich mich an den Workflow halten, den ich hier zum ersten Mal ausprobiert habe:  
  
Für die Präsentation habe ich ein Repository auf [GitHub](https://github.com/) angelegt. Das Repository ist [heinzwittenbrink/slides-csandtc: Slides on content strategy and technical communication](https://github.com/heinzwittenbrink/slides-csandtc). Um etwas via Github Pages zu veröffentlichen, muss man eine Branch namens `github pages` anlegen. In diese Branch checke ich die jeweils neueste Version meiner Präsentation ein, und zwar als [Markdown](https://daringfireball.net/projects/markdown/)\-Datei und als damit produzierte HTML-Version. Der Titel der HTML-Version ist `index.html`. Das von Github selbst gerenderte Markdown-File kann man sich hier anschauen: [slides-csandtc/ted2.md at gh-pages · heinzwittenbrink/slides-csandtc](https://github.com/heinzwittenbrink/slides-csandtc/blob/gh-pages/ted2.md), die ungerenderte Version hier: [https://raw.githubusercontent.com/heinzwittenbrink/slides-csandtc/gh-pages/ted2.md](https://raw.githubusercontent.com/heinzwittenbrink/slides-csandtc/gh-pages/ted2.md).  
Um die Präsentation zu erstellen habe ich [reveal.js](http://lab.hakim.se/reveal-js/#/) verwendet. Aus der Markdown-Version konvertiere ich sie mit [Pandoc](https://pandoc.org/). Wie man das macht, ist [hier](https://github.com/jgm/pandoc/wiki/Using-pandoc-to-produce-reveal.js-slides) einfach beschrieben. Ich habe lokal mit dem [GitHub Desktop](https://desktop.github.com/) gearbeitet und die Markdown-Datei selbst mit dem [iA Writer](https://ia.net/writer/) geschrieben. Wahrscheinlich werde ich anders vorgehen, wenn ich mich mit Github besser auskenne.

## Vorteile:

1. Die Präsentation selbst ist sauberes HTML, sie funktioniert auf jedem Gerät, und ich kann ihr Layout leicht via CSS verändern.
2. Zum Schreiben und Editieren der Präsentation brauche ich nur eine einfach strukturierte Text-Datei.
3. Ich kann verschiedene Versionen der Präsentation leicht managen; außerdem ist die Bearbeitung transparent, da das Repository offen ist.
4. Ich bin von keinem Anbieter abhängig; ich kann alle Daten leicht transferieren, sollte ich irgendwann nicht mehr Github verwenden.

## Schwierigkeiten:

Ich habe ein paar Tage gebraucht, um zu diesem Workflow zu kommen. Mir war erst nicht klar, dass man eine reveal.js-Version direkt mit Pandoc erzeugen kann. Ich habe zuerst auch nicht verstanden, dass Github Pages statische Seiten publiziert, dass man also die HTML-Version nicht dynamisch auf dem Server aus der Markdown-Datei erzeugen kann. Einige Posts zur lokalen Installation vor reveal.js sind für Nicht-Techies schwierig nachzuvollziehen, weil sie auf einen lokalen Webserver ausgerichtet sind, den man aber nicht braucht, wenn man mit Github-Pages publiziert. Schwierigkeiten hatte ich auch mit den Hierarchie-Ebenen der Präsentation. Man muss sich an die Regeln von Pandoc halten, siehe dazu [Level 1 and level 2 slides in reveal.js using pandoc](https://stackoverflow.com/questions/30988306/level-1-and-level-2-slides-in-reveal-js-using-pandoc/31778080). Das Ergebnis ist dann eine sauber strukturierte Präsentation.

## Update, 17.3.2019

Ich arbeite jetzt mit einem Custom-Stylesheet und verwende keine lokale reveal.js-Version mehr. Das Kommando zur Erstellung einer Präsentation ist im Augenblick (für eine Präsentationsvorlage namens `intro-deutsch.md`):

`pandoc -t revealjs -s -o index.html intro-deutsch.md -V revealjs-url=https://revealjs.com -V theme=white --css https://heinzwittenbrink.github.io/styles/customizations.css`

## Update, 8.11.2019

Um eine Bibliographie anzuschließen, muss ich im Terminal bei dem Befehl für die Konvertierung `--filter pandoc-citeproc` ergänzen (wobei `pandoc-citeproc` installiert sein muss, nicht einfach `pandoc`). In den Metadaten des Markdown-Dokuments füge z.B. ich hinzu:

`bibliography: introtocontentmarketing.bib`

`csl: apa.csl`

`link-citations: true`

Die Verlinkung der Zitate mit der Bibliographie funktioniert bei reveal allerdings nicht. Ich habe sie in den Metadaten für Konvertierungen zu HTML- bzw. PDF-Dokumenten hinzugefügt.
