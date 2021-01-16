---
title: "Emacs mit deutschen Umlauten"
date: "2005-03-01"
tags: 
  - "tools"
---

Frank Schoetzau beschreibt, wie man unter OS X den [Emacs auf deutsche Umlaute](http://www.schoetzau.com/comments.php?id=141_0_1_0_C) einstellt (via [SWR](http://www.schockwellenreiter.de/2005/02/28.html#escapeMetaAltControlShift)). Auf dem G5-iMac, auf dem ich arbeite, reichen folgende Zeilen für die GUI-Version aus:  

  
(set-frame-font "fontset-mac")  
(set-keyboard-coding-system 'mac-roman)  

  
Den Emacs habe ich entsprechend Andrew Chois [Anleitung](http://members.shaw.ca/akochoi-emacs/stories/obtaining-and-building.html) kompiliert. Wenn ich einen zweiten Frame öffne, werden dort allerdings keine Umlaute angezeigt.
