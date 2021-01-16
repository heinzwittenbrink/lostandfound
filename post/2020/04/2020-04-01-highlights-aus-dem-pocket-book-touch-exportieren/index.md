---
title: "Highlights aus dem Pocket Book Touch exportieren"
date: "2020-04-01"
categories: 
  - "schreiben-und-hypermedia"
tags: 
  - "epub"
---

Ich habe mir kurz nach Weihnachten einen [PocketBook Touch HD 3](https://www.pocketbook-int.com/at/products/pocketbook-touch-hd-3 "PocketBook Touch HD 3 - PocketBook") gekauft, und ich lese längere Texte sehr gerne damit (z.B. Masterarbeiten, die unsere Studierenden als epub-Files abgeben). Einziges Problem: Highlights (Stellen, die ich mir anstreiche) werden nicht vom Reader mit den [Apps](https://pocketbook.ch/de-ch/app "PocketBook Reader") auf Mobiltelefon und Computer synchronisiert. Es ist aber leicht, die Highlights zu exportieren, wenn man das Gerät an einen Rechner anschließt und die Datenbank (`system/config/books.db`) im Terminal mit sqlite3 öffnet. (**Update, 3.Mai 2020:** Sicherheitshalber kopiere ich die Datei vorher auf meinen Rechner.) Eine HTML-Tabelle mit allen Highlights kann man mit folgendem Kommando produzieren:

```
echo "<HTML><BODY><TABLE>"$(sqlite3 --header --html books.db "select Title, Authors, json_extract(Highlight, '$.text') as Text from Books inner join (select OID as BookID, Highlight from Items inner join (select ParentID, Highlight from Items inner join (select ItemID, Val as Highlight from Tags where TagID = 104 and Val <> '{\"text\":\"Bookmark\"}') as Highlights on Highlights.ItemID = OID) as Highlights on Highlights.ParentID = OID) as Highlights on BookID = OID;")"</TABLE></BODY></HTML>" > highlights.html
```

Ich habe es [hier](https://www.mobileread.com/forums/showthread.php?t=281744&page=3 "Pocketbook Annotations Extraction - Page 3 - MobileRead Forums") gefunden, danke [retrography](https://www.mobileread.com/forums/member.php?s=5fc0e695e836359e81206b45db955a49&u=295613 "Userprofil retrography bei mobilread.com")!
