---
title: "Copy URL+ für Markdown anpassen"
date: "2007-07-06"
tags: 
  - "tools"
---

Aus der Serie _Wie schreibt man am einfachsten Hypertext_:

(**Update:** Siehe [Markus' Kommentar](http://heinz.typepad.com/lostandfound/2007/07/copy-url-fr-mar.html#c75077518)! Wahrscheinlich ist [Make Link](http://www.soylentred.net/projects/make-link "SoylentRed.net | Make Link") die bessere Alternative.)

Sollte noch jemand mit [Copy URL+](https://addons.mozilla.org/de/firefox/addon/129 "Copy URL + :: Firefox Add-ons") ([hier](http://btcorp.dyndns.org/Tools/FireFoxExtensions/FF_2.0_extensions/ "Index of /Tools/FireFoxExtensions/FF_2.0_extensions") gibt es eine Firefox 2-kompatible Version) und [Markdown](http://daringfireball.net/projects/markdown/ "Daring Fireball: Markdown") arbeiten: Schreibt man die folgenden Ergänzungen in die Datei _user.js_ , kann man durch einen Klick auf die rechte Maustaste im Firefox markierten Text in ein Markdown-Link verwandeln; entweder für ein direktes Link oder für ein `blockquote`\-Element mit einem Zitat:

```
user_pref('copyurlplus.menus.1.label', 'Simple Markdown Link');
user_pref('copyurlplus.menus.1.copy', '[%SEL_HTMLIFIED%]
(%URL_HTMLIFIED% "%TITLE_HTMLIFIED%")');
user_pref('copyurlplus.menus.2.label', 'Extended Markdown Link');
user_pref('copyurlplus.menus.2.copy', '[%TITLE_HTMLIFIED%]
(%URL_HTMLIFIED% "%TITLE_HTMLIFIED%"):nn>%SEL_HTMLIFIED%nn');
```

(Das vor `(%URL` steht nur für die Fortsetzung der zweiten Zeile; Dokumentation zum Erweitern von Copy URL+ [hier](http://copyurlplus.mozdev.org/customize.html "mozdev.org - copyurlplus: customize") und [hier](http://www.mvps.org/dmcritchie/firefox/copyurlplus.htm "COPYURL Plus, format a link for HTML"))

Simplere Methoden, um zum selben Ziel zu kommen, sind willkommen!
