---
title: "Such-Operatoren"
date: "2005-10-19"
tags: 
  - "suche"
---

[Dieser Eintrag](http://heinz.typepad.com/lostandfound/2005/10/suchoperatoren.html#more) gibt einen Überblick über Such-Operatoren bei verschiedenen Suchmaschinen. Ich dokumentiere sie vor allem für eine Lehrveranstaltung zum Thema "Archivtechniken". Ich möchte den Eintrag schrittweise erweitern und dann aktualisieren, wenn ich auf neue oder geänderte Operatoren stoße.

**Letzte Aktualisierung: 19.10.2005**

Google dokumentiert die verschiedenen Operatoren, mit denen sich Suchen einschränken lassen, inzwischen auf einer eigenen Seite: [Google Guide: Using Search Operators (Advanced Operators)](http://www.googleguide.com/advanced_operators.html) Lange brauchte man Texte wie [Google Hacks](http://www.oreilly.com/catalog/googlehks/), um diese Funktionen zu finden.

Yahoo erläutert seine Such-Operatoren (deutlich weniger) auf einer Seite über [Advanced Search](http://help.yahoo.com/help/us/ysearch/basics/basics-08.html).

Wesentlich mehr Möglichkeiten erklärt das Weblog zur MSN Suche: [New Operators Explained](http://blogs.msdn.com/msnsearch/archive/2005/06/24/432439.aspx). Bei MSN kann man z.B. nach Seiten suchen, die auf eine bestimmte Seite linken und bestimmte Termini enthalten: Der Suchstring inbody:miserable inbody:failure link:www.whitehouse.gov/president/gwbbio.html führt zu Seiten, die auf die offizielle Biografie George Bushs linken und den Ausdruck "failure" enthalten. Inzwischen sind die Operatoren **feed:** und **hasfeed:** hinzugekommen, mit denen sich in Feeds und nach Feeds suchen lässt. \[[MSN Searches RSS Deeper - Robin Good's Latest News](http://masternewmedia.org/RSS_search/RSS_search_tools/MSN_RSS_search_improves_capabilities_20050831.htm)\]

In der folgenden Tabelle liste ich die Operatoren auf, die ich gefunden habe. In der ersten Version beschränke ich mich auf die special operators und lasse die Booleschen Operatoren weg.

  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  
  

  

| Operator | Bedeutung | Beispiel | Suchmaschine(n) |
| --- | --- | --- | --- |
| **filetype:** | Suche nach einem bestimmten Dateityp | filetype:pdf | Google |
| **cache:** | Suche in Googles Cache; Suchtermini werden farbig unterlegt | cache:www.kleinezeitung.at voves | Google |
| **allintitle:** | Suche nach Vorkommen im Titel einer Seite | allintitle: rss atom | Google |
| **allintext:** | Suche nach Vorkommen im Text einer Seite | allintext: voves schützenhofer | Google |
| **allinurl:** | Suche nach Vorkommen im URL einer Seite | allinurl: rss syndication | Google |
| **allinanchor:** | Suche nach Vorkommen in den Links zu einer Seite | allinanchor: rss atom | Google |
| **site:** | Suche innerhalb einer Domain | schützenhofer site:www.kleinezeitung.at | Google |
| **related:** | Suche nach ähnlichen Seiten | related:www.kleinezeitung.at | Google |
| **link:** | Suche nach Links zu einer Seite | link:www.fh-joanneum.at | Google |
| **safesearch:** | Suche nach für Kinder sicheren Seiten |  | Google |
| **author:** | Beschränkt Suche innerhalb der Google Groups auf Seiten, die von einem bestimmten Autor stammen |  | Google |
| **bphonebook:** | Suche in business white page listings |  | Google |
| **define:** | Suche nach Definitionen eines Ausdrucks | define:leather, definier:HTML | Google |
| **ext:** | Alternative zu filetype: |  | Google |
| **id:** | Alternative zu info: |  | Google |
| **group:** | Suche innerhalb bestimmter Google Groups |  | Google |
|   
**inanchor:**  
 | Suche nach Termini in den Links zu einer Seite |  | Google |
| **info:** | Ergänzende Informationen zu einer Seite | info:www.fh-joanneum.at | Google |
| **insubject:** | Einschränkung auf bestimmte Themen innerhalb der Google Groups |  | Google |
| **intext:** | Suche innerhalb des Texts von Seiten |  | Google |
| **intitle:** | Suche innerhalb der Titel von Seiten |  | Google |
| **inurl:** | Suche innerhalb der URLs |  | Google |
| **location:** | Suche innerhalb der Google News nach Seiten von bestimmten Orten |  | Google |
| **movie:** | Suche nach Informationen zu Filmen | movie:Titanic | Google |
| **msgid:** | Suche innerhalb der Google Groups nach Botschaften mit einer bestimmten id |  | Google |
| **phonebook:** | Suche innerhalb von Telefonbüchern |  | Google |
| **rphonebook:** | Suche innerhalb von residential white page listings (Adressbüchern) |  | Google |
| **source:** | Einschränkung der Suche in den Google News auf bestimmte Quellen | Merkel source:new\_york\_times(in der amerikanischen Version) | Google |
| **stocks:** | Interpretiert den Rest der Abfrage als Ticker Symbole |  | Google |
| **store:** | Beschränkte eine Frogle-Suche auf die ID eines bestimmten Geschäfts |  | Google |
| **weather:** | Sucht nach dem Wetter an einem bestimmten Ort | weather:graz | Google |
