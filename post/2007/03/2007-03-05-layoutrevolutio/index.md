---
title: "\"Layout-Revolution&quot, Unterricht, Drupal"
date: "2007-03-05"
tags: 
  - "css"
  - "studium"
  - "tools"
---

Vor Monaten bin ich auf einen [Hinweis](http://meyerweb.com/eric/thoughts/2005/11/01/layout-revolution/ "Eric's Archived Thoughts: Layout Revolution") Eric Meyers auf Alex Robinsons [In search of the One True Layout](http://www.positioniseverything.net/articles/onetruelayout/ "Introduction - In search of the One True Layout") gestoßen. Meyer bezeichnet Alex Robinsons Methode CSS-Layouts zu definieren als "Layout-Revolution" und ersten zufriedenstellenden Versuch, mit CSS beliebige Grid-orientierte Layouts zu erzeugen, also mit Spalten und horizontal angeordneten Blöcken zu arbeiten.

Am Wochenende habe ich Robinsons Artikel zum ersten Mal gelesen. Die Methoden, die er vorschlägt, sind tatsächlich verblüffend simpel. Bei Kolumnen werden z.B. einfach `float`s verwendet, deren Position durch einen negativen Wert für `margin` festgelegt wird. Dadurch ist das Layout unabhängig von der Position des Abschnitts im Quelltext. Auch bei den übrigen Komponenten von Robinsons Layout-Konzept besteht das Hauptziel darin, das Layout konsequent vom Quelltext zu trennen. Der HTML-Autor kann so auf Markup verzichten kann, das nur aus gestalterischen Gründen eingefügt wird. Für ein Layout, das in allen gängigen Browsern funktioniert, braucht Robinson lediglich ein wrapper-`div` und eine Klasse (`vertical align`).

Robinsons Technik interessiert mich aus zwei Gründen: Ich hoffe, dass sie es leichter macht, HTML und CSS zu unterrichten, und ich möchte sie auch für Projekte verwenden. Zuerst zum Unterricht:

### "One True Layout" im Unterricht?

Bisher ist die Erstellung von anspruchsvollen CSS-Layouts, die in allen Browsern funktionieren, a pain in the ass. Seit Jahren versuche ich Studenten davon zu überzeugen, die Auszeichnung von Inhalten via HTML und die optische Gestaltung via CSS voneinander zu trennen, also Webstandard-konform zu arbeiten. Nicht-Informatikern fällt die Unterscheidung der beiden Ebenen meist sehr schwer. Wenn sie aber schon reines HTML (und das noch ohne einen grafischen Editor) produzieren, möchten sie wenigstens bestimmen können, wie der Text in einem Browser aussieht. Um dabei auch nur in die Nähe der Qualität von Layouts zu kommen, die sich für gedruckte Dokumente mit jedem Textverarbeitungsprogramm zusammenklicken lassen (und die man auch mit grafischen HTML-Editoren leicht zusammenbringt), brauchen sie CSS-Kenntnisse, die sich Laien kaum vermitteln lassen. Für mich widerspricht die Komplexität von CSS dem Ziel des Web, jedem das Publizieren zu ermöglichen. Natürlich ist der Hauptgrund für die Schwierigkeit von CSS, dass alle Browser, vor allem der IE 5 und 6, hoffnungslos buggy sind. Aber auch wenn sie das nicht wären: Wer CSS richtig verwenden will, muss verstehen, wie ein Layout berechnet wird. Er muss wenigstens eine Ahnung davon haben, was ein normal layout flow ist, um Eigenschaften wie `float` und `position` zu benutzen. Damit wird CSS zu einer Angelegenheit von Spezialisten.

Zurück zu Alex Robinson: Sein Aufsatz lässt mich hoffen, dass ich mir das Unterrichten von CSS erlichtern kann. Zwar dürfte ein Laie kaum verstehen, wie er z.B. die Bugs in älteren Versionen von [Opera](http://www.opera.com/products/ "Opera products") austrickst. Man kann aber fast beliebige Layouts produzieren, indem man nur wenige Parameter in Robinsons Stylesheets verändert. (Ich habe es selbst noch nicht probiert, aber ich vertraue Erich Meyer). Für den Unterricht hätte ich damit wenigstens eine Vorlage, in die ich schrittweise einführen kann. Das Ziel kann nur sein, den Ansatz zu verstehen. Robinson warnt zu Recht davor, seine Lösung einfach zu kopieren.

### YAML for Drupal

Zu Projekten (und damit wieder zum Unterricht): Ich versuche gerade, [Drupal](http://drupal.org/ "drupal.org | Community plumbing") für Studentenprojekte zu benutzen. Für Drupal 4.7 gibt es das Thema [Fern](http://drupal.org/node/65931 "Fern | drupal.org"), das Robinsons Methode umsetzt. Für Drupal 5 habe ich nichts Entsprechendes gefunden, dafür aber [YAML für Drupal](http://www.yaml-fuer-drupal.de/ "YAML für Drupal - Yet Another Multicolumn Layout") von [Dirk Jesse](http://www.highresolution.info/ "High Resolution | Webdesign und digitale Bildgestaltung - Home"). Jesse hat das von ihm entwickelte [YAML](http://www.yaml.de/ "Yet Another Multicolumn Layout | Ein (X)HTML/CSS Framework")\-Framework für eine Reihe von Drupal-Themen verwendet. Auch YAML verzichtet auf Layout-bezogenes Markup und nimmt die Methoden Robinsons auf. Ich habe mir die Stylesheets noch nicht angesehen; die Installation war problemlos, und out-of-the-box steht einem eine ganze Serie von Webstandard-konformen Layouts zur Verfügung. Mit denen möchte ich in den nächsten Wochen experimentieren.

### Abschlussbemerkung:

Vor zwei Jahren habe ich Alex Robinsons Technik nicht und Drupal kaum gekannt. Wenn ich sie im Unterricht verwende, unterrichte ich Dinge, die ich mir selbst beibringe. Vielleicht ist das ein Problem. Ich sehe es eher als ein Privileg.
