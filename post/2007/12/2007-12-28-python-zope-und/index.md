---
title: "Python, Zope und Plone unter Leopard aus den Quellen installieren"
date: "2007-12-28"
categories: 
  - "allgemein"
tags: 
  - "tools"
---

Wenn andere Männer in meinem Alter wollen, dass stundenlang nichts passiert, gehen sie wahrscheinlich angeln. Ich beschäftige mich dagegen damit, Open Source Software auf einem Mac zu installieren. Hier ein Bericht über eine [Plone](http://plone.org/ "Plone CMS: Open Source Content Management")\-Installation, die mich insgesamt fast einen Tag beschäftigt hat — nicht zuletzt, weil ich nicht gründlich genug gegoogelt habe, um Hilfen zu finden.

Nach einer ganzen Reihen von fehlgeschlagenen Versuchen ist es mir gelungen, eine ältere Version von Plone/Zope unter Leopard (OS X 10.5) aus den Quellen zu installieren. Ich brauche die Kombination von Plone 2.1.2, Zope 2.8.6 und Python 2.4, um an einem seit Jahren nicht abgeschlossenenen Projekt weiterzuarbeiten. Für die Verzeichnisstruktur und die Optionen bei der Installation habe ich mich an [Installer Plone/Zope/Python à partir des sources](http://www.sebastien-verbois.be/plone/installation-configuration-administration/installer-plone-25/ "Installer Plone/Zope/Python à partir des sources — www.sebastien-verbois.be") von Sébastien Verbois gehalten (auch mit geringen Französisch-Kenntnissen verständlich). Die Verzeichnisstruktur, die Sébastien vorschlägt, eignet sich gut, um mehrere Versionen vom Python, Zope und Plone nebeneinander zu installieren und dabei die Übersicht zu bewahren. An zwei Stellen hatte ich auf meinem neuen MacBook Probleme. Es gelang mir zunächst nicht, Python zu kompilieren, bis ich bei [Wolfgang Reutz](http://wolfgang.reutz.at/blog/2007/10/29/compile-python-244-on-mac-os-x-105-leopard/ "#define SETPGRP_HAVE_ARG 1"), auf den einfachen Hinweis stieß, nach dem Aufruf von **configure** die Zeile

```
#define SETPGRP_HAVE_ARG 1
```

in die Datei **pyconfig.h** einzufügen. Der Rest der Installation lief dann problemlos. Allerdings konnte ich mit dem Ergebnis wenig anfangen, weil das kompilierte Python im interaktiven Modus bei der zweiten Eingabe immer wieder abstürzte. (Man kann Zope über den Befehl `zopectl debug` so starten, dass sich die Zope-Datenbank interaktiv ansprechen lässt.) Eine Lösung für dieses Problem habe ich zum Glück bei [Andreas Jung](http://blog.zopyx.com/blog_ajung/archive/2007/11/02/compiling-readline-support-for-python-on-macosx "Compiling readline support for Python on MacOSX — Portal") gefunden. Man muss via [MacPorts](http://www.macports.org/ "The MacPorts Project -- Home") eine eigene Version von [Readline](http://tiswww.case.edu/php/chet/readline/rltop.html "The GNU Readline Library") installieren (der Befehl lautet `sudo port install readline`) und nach dem Aufruf von **configure**

```
CC = gcc -I/opt/local/include -L/opt/local/lib
```

in das **Makefile** eintragen. (Für Python 2.5 ist etwas mehr nötig, siehe Andreas Jung.)

Danach hat alles geklappt. Jetzt hoffe ich nur, dass ich zur Arbeit mit der Zope-Datenbank selbst ähnlich hilfreiche Hinweise finde.
