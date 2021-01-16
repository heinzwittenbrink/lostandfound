---
title: "Mit Markdown HTML schreiben"
date: "2007-04-10"
tags: 
  - "tools"
---

Typepad bietet seit einiger Zeit auch an, mit [Markdown](http://daringfireball.net/projects/markdown/ "Daring Fireball: Markdown") zu bloggen. Ich experimentiere im Augenblick damit und bin von dieser Schreibtechnik sehr angetan. Mit Markdown formatiert man einen Text ähnlich wie ein Email; er wird dann in korrektes XHTML konvertiert. Die Markdown-Formatierungsregeln sind sehr einfach und [übersichtlich dokumentiert](http://daringfireball.net/projects/markdown/syntax "Daring Fireball: Markdown-Syntax"); deutsch [hier](http://liepins.org/de/markdown-syntax-deutsch/ "Markdown-Syntax Deutsch"), sehr lesbar [auch hier](http://adlcommunity.net/help.php?file=markdown.html "adlCommunity: Enhancing Text with Markdown"). Text, der zwischen Leerzeilen eingeschlossen ist, wird z.B. in das HTML-Element `p` konvertiert. Überschriften kann man je nach Hierarchieebene mit einem (für `h1`) bis sechs `#` (für `h6`) beginnen lassen. Für Hyperlinks setzt man den zu verlinkenden Text in eckige Klammern und dahinter wieder in eckige Klammern ein Zahl oder ein Kürzel (z.B.: `[Markdown][1]`). Am Ende des Text notiert man dann das Linkziel und den Titel im Email-Stil:

```
[1]:http://daringfireball.net/projects/markdown/  "Daring Fireball:Markdown"
```

(Es gibt auch andere Möglichkeiten, mit Markdown Links zu schreiben.)

Markdown vereinfacht es, Hypertext zu schreiben. Genauso wichtig ist für mich, dass es das Lesen des Quelltexts erleichtert und damit die Zahl der Korrekturen reduziert.

Markdown ist minimalistisch: Es gibt nur für die gängigsten HTML-Elemente einen Markdown-Ersatz. Für die übrigen fügt man einfach HTML in den Markdown-Quelltext ein.

Im Augenblick quäle ich meine Studenten damit, dass sie HTML-Quelltext schreiben müssen. Ich möchte darauf auch in Zukunft nicht verzichten, damit sie lernen, wie HTML funktioniert und auf was man achten muss, damit ein Text z.B. auf unterschiedlichen Displays lesbar ist. Als Hilfsmittel zum Verfassen von Texten werden ich ihnen in Zukunft aber wohl Markdown vorschlagen. Allerdings kenne ich die Alternativen wie [Textile](http://www.textism.com/tools/textile/ "Textism: Tools: Textile"), [StructuredText](http://zwiki.org/StructuredText "zwiki org: StructuredText") und [ReStructuredText](http://docutils.sourceforge.net/rst.html "Sourceforge: reStructuredText") nicht gut.
