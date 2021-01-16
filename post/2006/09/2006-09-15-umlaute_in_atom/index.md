---
title: "Umlaute in Atom-Feeds von Typepad"
date: "2006-09-15"
tags: 
  - "syndication"
  - "tools"
---

Ein wahrscheinlich selten auftretendes Problem: Die Atom-Feeds, die [Typepad](http://www.typepad.com/) mit seinem Default-Template produziert, löschen Umlaute (und wahrscheinlich andere Nicht-ASCII-Zeichen) in den Elementen `summary` und `title`. Man muss im Template in den beiden MT-Tags `remove_html="1"` statt `"0"` angeben, um die Umlaute zu erhalten.
