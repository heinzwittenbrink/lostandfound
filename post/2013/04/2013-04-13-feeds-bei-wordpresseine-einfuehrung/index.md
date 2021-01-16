---
title: "Feeds bei Wordpress—eine Einführung"
date: "2013-04-13"
categories: 
  - "web"
tags: 
  - "change11"
  - "mmc13"
---

Warum und wie publiziert man RSS-Feeds mit Wordpress, und wie kann man Feeds in Wordpress einbinden?—Dieses Post gehört zu unserer Lehrveranstaltung [Webbasiertes Arbeiten](http://www.fh-joanneum.at/aw/home/Studienangebot_Uebersicht/department_medien_design/jpr/Studium/~urn/JPR_lvdetails/?alvid=4325968878&lan=de "Webbasiertes Arbeiten 2 |  Journalismus und Public Relations (PR) | FH JOANNEUM Gesellschaft mbH :: University of applied sciences"). In diesem Kurs benutzen wir Wordpress als Beispiel, um Werkzeuge zum Arbeiten und zum Publizieren im Web kennenzulernen. Wir haben uns schon in einer Session mit Plugins im allgemeinen beschäftigt. Hier geht es um den ersten wirklichen Anwendungsfall: Newsfeeds oder RSS-Feeds—kurz: Feeds.

### Wozu brauche ich RSS und Atom?

Ich beginne mit Beispielen. Wo benutze ich selbst RSS und Atom? Was diese Bezeichnungen bedeuten, dazu später! Gleich zu Beginn die Zusammenfassung: Feeds mit RSS und Atom sind für mich eines der wichtigsten Mittel, um regelmäßig Informationen aus dem Web zu bekommen. Außerdem verwende ich sie, um Informationen aus verschiedenen Quellen zu republizieren, und dazu, Inhalte, die ich selbst veröffentliche, abonnierbar zu machen.

Ich höre mir morgens beim Frühstück, wenn ich Zeit habe, das [Ö1-Morgenjournal](http://oe1.orf.at/journale/ "oe1.ORF.at Journale") oder die [Nachrichten im Deutschlandfunk](http://www.dradio.de/nachrichten/ "Nachrichten vom 13.04.2013 18:00 - dradio.de") an. Ich mache dazu aber nicht das Radio an, sondern ich höre sie als Podcasts mit einer iPad-App: [Instacast](http://vemedio.com/products/instacast3 "Instacast 3 - The Next Generation - Vemedio"). Ich kann sie also hören, wann ich will. Podcasts basieren auf RSS. Instacast, meine [Podcatcher](http://www.podcast.de/software/podcatcher/ "Podcatcher - Software zum Abonnieren von Podcasts")\-App, bekommt von allen Podcasts, die ich abonniert habe, einen RSS-Feed mit Links zu Audio- oder auch Video-Dateien. Je nach Voreinstellung werden einige dieser Dateien automatisch heruntergeladen, andere nur dann, wenn ich sie hören will.

Zwei weitere mobile Apps, die für meinen alltäglichen News-Konsum wichtig sind: [Flipboard](http://flipboard.com/ "Flipboard") und [my6sense](http://www.my6sense.com/ "my6sense"). Beide verarbeiten RSS-Feeds, in diesem Fall aber Feeds mit Textinhalten. Ich habe viele Blogs und eine Reihe von Nachrichten-Sites abonniert und kann mich auf dem Smartphone uptodate halten, während ich zur Arbeit fahre.

Flipboard und my6sense greifen nicht direkt auf die Feeds zu, die ich abonniert habe, sondern bekommen sie aus dem [Google Reader](http://de.wikipedia.org/wiki/Google_Reader "Google Reader – Wikipedia"). Das wird sich bald ändern, denn Google [stellt den Reader Ende Juni ein](http://netzwertig.com/2013/03/14/am-1-juli-ist-schluss-das-ende-des-google-reader-ist-traurig-aber-zu-begruesen/ "Am 1. Juli ist Schluss: Das Ende des Google Reader ist traurig, aber zu begrüßen | netzwertig.com I Internetwirtschaft I Startups I Trends I Digitalisierung"). Bald wird man mit Flipboard direkt Newsfeeds abonnieren können.

Die Newsfeeds bei Flipboard und in jedem anderen Newsreader zeigen mir die Überschriften von Artikeln und Meldungen der Seiten, die ich abonniert habe. Meist bieten sie darüber hinaus auch den kompletten Inhalt.

Aus den Podcasts und Newsfeeds setze ich mir mein persönliches Nachrichtenmenü zusammen. Vor kurzem habe ich RSS aber auch verwendet, um für andere Nachrichtenquellen zusammenzufassen, also zum _Kuratieren_: Auf dem Wordpress-Blog des MOOC Maker-Kurses habe ich [eine Seite eingerichtet, die einen Überblick über die Blogposts der Kursteilnehmer gibt](http://howtomooc.org/mmc13-blog-aggregator/ "Blog-Aggregator - #MMC13 - der Open MOOC-Maker Course 2013"). Dazu werden Newsfeeds von Posts zusammengefasst (Fachausdruck: _aggregiert_), die mit dem Schlagwort _mmc13_ getaggt sind. Die meisten Blog-Systeme bieten nämlich für jedes Tag und für jede Kategorie einen eigenen Newsfeed an.

Schließlich publiziere ich auch RSS-Feeds. Mein eigenes Blog (also dieses hier) haben gerade 300 Leute über RSS abonniert. Auch alle möglichen anderen Spuren, die ich im Web hinterlasse, sind via RSS zu beziehen, z.B. [mein Tumblelog](http://enpassant.wittenbrink.net/rss "enpassant.wittenbrink.net/rss") oder die [Bookmarks, die ich bei Pinboard speichere](http://feeds.pinboard.in/rss/u:heinzwittenbrink/ "feeds.pinboard.in/rss/u:heinzwittenbrink/").

Ich könnte diese Reihe noch fortsetzen. Aber ich glaube, dass auch so deutlich wird: RSS erleichtert es enorm, Inhalte im Web zu publizieren und zu abonnieren

Für George Siemens [gehören zum Lernen im Web vier Komponenten](http://change.mooc.ca/how.htm "How This Course Works ~ #change11"):

1. aggregate,
2. remix,
3. repurpose,
4. feed forward.

Mit diesen vier Verben lässt sich auch das Publizieren im Web beschreiben. Für das ganze Quartett sind Feeds die Basis, und RSS ist das wichtigste der Formate für Feeds

### Was ist überhaupt RSS?

Die Beispiele zeigen schon: RSS-Feeds kann ich mit Newsreadern und Podcatchern abonnieren. RSS ist das Format, das diese Anwendungen verstehen. Auf die vielen Programme, die RSS verarbeiten, will ich hier nicht eingehen. Ich habe schon erwähnt, dass es die bisher wichtigste von ihnen, den Google Reader, [nicht mehr lange geben wird](http://netzwertig.com/2013/03/14/am-1-juli-ist-schluss-das-ende-des-google-reader-ist-traurig-aber-zu-begruesen/ "Am 1. Juli ist Schluss: Das Ende des Google Reader ist traurig, aber zu begrüßen | netzwertig.com I Internetwirtschaft I Startups I Trends I Digitalisierung"). Die Einstellung des Google Readers sagt einiges über die Besonderheiten von RSS aus. Google macht, vereinfacht gesagt, den Google Reader dicht, um sein eigenes, proprietäres Produkt zum Produzieren und Abonnieren von News, nämlich Google+, nicht selbst zu schädigen. Auch auf Google+ kann man Nachrichten beziehen und sich zusammenstellen, und man kann auch über Google+ Texte und Medien, die man produziert, teilen. Das Format von Googe+ kontrolliert aber nur Google, und Google kann entscheiden, ob externe Anwendungen auf seine Inhalte zugreifen dürfen oder nicht. Genauso ist es bei Facebook und Twitter. Sie bieten Newsfeeds an, aber sie verwenden proprietäre Technologien dafür.

RSS ist dagegen ein offenes, standardisiertes Format. Es gehört niemand. Jeder kann RSS-Feeds produzieren und Newsreader programmieren. Es gibt keine Firma, die RSS kontrolliert.

RSS ist wie HTML ein Textformat. Wie ein HTML-Dokument enthält ein RSS-Dokument durch Spitzklammern abgegrenzte Tags, wobei die Namen dieser Tags etwas über ihre Funktion sagen. RSS-Feeds enthalten Informationen über den ganzen Newsfeed, also über seinen Titel, seinen Urheber, die letzte Aktualisierung und seinen URL, und über die einzelnen Nachrichten. Außerdem gibt es viele Zusatzinformationen (z.B. zu den Rechten an den Inhalten) und, wie schon erwähnt, optional Links zu Medien (bei Podcasts) und die kompletten Inhalte. (Zum Format siehe die [Wikipedia](http://de.wikipedia.org/wiki/RSS "RSS – Wikipedia") und viele weitere Quellen!)

[Atom](http://de.wikipedia.org/wiki/Atom_(Format) "Atom (Format) – Wikipedia")\-Feeds unterscheiden sich in ihrem Markup von RSS-Feeds, aber nicht in ihrer Funktion. Sie gelten allgemein als technisch sauberer, aber für den Benutzer sind die Unterschiede nicht spürbar. Die meisten Programme zur Produktion und zum Darstellen von Feeds verstehen beide Formate (wobei übrigens RSS selbst wiederum in verschiedenen Versionen vorliegt).

### Mit Wordpress Feeds publizieren

Wie jedes gute Content Management-System erzeugt Wordpress Feeds, und zwar RSS- und Atom-Feeds für alle Blogposts. Wir haben schon gesehen, dass es außerdem u.a. Feeds für Kategorien und Tags gibt. Die RSS-Feeds sind normalerweise bei allen Wordpress-Blogs unter demselben URL erreichbar. Wenn man diesen URL in einen Newsreader (wenn man podcastet, in einen Podcatcher wie iTunes) eingibt, kann man das Blog abonnieren. Meist reicht es, die Blogadresse selbst zu abonnieren. Im Head der HTML-Version gibt es ein Link zu den Newsfeeds, das der Newsreader erkennt.

Wichtig: Man kann auch die Kommentare eines Blogs und die Kommentare zu einem einzelnen Post via Feed abonnieren.

Die meisten Wordpress-Themen enthalten ein Link zum RSS-Feed. Vielfach verwendet man statt des Textlinks oder zusätzlich zu ihm ein Symbol, das stilisierte Radiowellen zeigt. Da Newsreader (und auch Browser) RSS-Feeds aber selbst erkennen, ist dieses Link nicht mehr unbedingt nötig.

Man muss sich also, wenn man bloggt, nicht unbedingt um RSS kümmern. Es wird ja automatisch mitproduziert. Trotzdem sollte man aber wissen, dass man einen RSS-Feed publiziert. Viele Blogs haben mehr Abonnenten des RSS-Feeds als Leser, die direkt auf die Seite kommen. Das bedeutet unter anderem, dass die Leser einen großen Teil des Layouts gar nicht oder nur selten sehen.

Wichtig: In den Einstellungen kann man entscheiden, ob der Feed die kompletten Posts oder nur einen Teaser enthalten soll. Wie lang dieser Teaser ist, lässt sich festlegen, indem man ein `<!--more-->` in den Quelltext des Posts einfügt. Allerdings sorgt dieser Einschub auch dafür, dass auf der Startseite des Blogs nur der Teaser dargestellt wird (siehe [hier](http://forum.wpde.org/konfiguration/39898-hilfe-zu-rss-feed-einstellungen.html "Hilfe zu RSS Feed Einstellungen")).

Grundinformationen zu den verschiedenen Feeds, die Wordpress generieren kann, und zu ihren URLs findet man [hier](http://codex.wordpress.org/WordPress_Feeds "WordPress Feeds « WordPress Codex"). Eine sehr elementare Einführung in Wordpress-Feeds ist [RSS Feed für euren WordPress Blog](http://www.blog-tips.de/rss-feed-wordpress-blog/ "RSS Feed für euren WordPress Blog - Blog Tips").

Wenn man die Abonnentenzahl seines Blogs steigern möchte, und wenn man wissen will, welchen Erfolg man mit seinem Blog hat, sollte man sich allerdings genauer mit den RSS-Feeds beschäftigen. Das wichtigste Hilfsmittel ist dabei für mich ein weiteres Google-Tool namens [FeedBurner](https://accounts.google.com/ServiceLogin?service=feedburner&continue=http%3A%2F%2Ffeedburner.google.com%2Ffb%2Fa%2Fmyfeeds&gsessionid=zsMoJX7d_JdZHl-wYb8yIw "Google FeedBurner").

Ob Feedburner von Google nach dem Ende des Reader weiterbetrieben wird, [ist fraglich](http://techcrunch.com/2013/03/13/the-google-reader-shutdown-is-yet-another-nail-in-feedburners-coffin/ "The Google Reader Shutdown Is Yet Another Nail In Feedburner’s Coffin | TechCrunch"). Neulich sah es schon einmal kurz so aus, als würde Google Feedburner einstellen. Die Nachricht [erwies sich aber als falscher Alarm](http://stadt-bremerhaven.de/nein-google-feedburner-macht-nicht-dicht/ "Nein, Google Feedburner macht nicht dicht"). Siehe für alle Fälle: [5 Alternativen zu FeedBurner](http://www.perun.net/2012/09/24/5-alternativen-zu-feedburner/ "5 Alternativen zu FeedBurner » WordPress & Webwork").

Feedburner hat mehrere nützliche Funktionen:

1. Es ersetzt den vom CMS, in unserem Fall also von Wordpress, produzierten RSS-Feed durch Newsfeeds in allen üblichen Formaten, so dass jeder mögliche Newsreader die optimale Version bekomm.
    
2. Es trackt die Benutzung des Feeds. Man erfährt nicht nur, wie viele Abonnenten man hat, sondern auch, wer auf einen Eintrag klickt und welchen Newsreader die Abonnenten benutzen.
    
3. Es ermöglicht es, den Newsfeed zu optimieren (z.B. mit zusätzlichen Informationen zu Lizenzen, Geoinformationen u.ä. auszustatten) und generiert z.B. auch Emails, über die man das Blog ebenfalls abonnieren kann.
    

Um Feedburner zu nutzen, muss man diesen Dienst in seinem Google-Profile aktivieren und dort die Adresse des RSS-Feeds des eigenen Blogs angeben. Dann sollte man bei Wordpress das [Feedburner Plugin](http://wordpress.org/extend/plugins/feedburner-plugin/ "WordPress › FD Feedburner Plugin « WordPress Plugins") installieren. Es sorgt dafür, dass der von Feedburner produzierte Feed abonniert wird, wenn jemand im Blog auf den RSS-Link klickt. Sonst hat man zwei Feeds (einen originalen, einen von Feedburner), so dass die Zählung bei Feedburner nicht alle Abonnenten erfasst.

Man kann den RSS-Feed des eigenen Blogs übrigens auch in seinen Facebook-Newsfeed integrieren. Es gibt dazu verschiedene Facebook-Apps. Mit [NetworkedBlogs](https://www.facebook.com/networkedblogs "(2) NetworkedBlogs") nimmt man auf Facebook an einer Blogger-Community teil. [RSS Graffiti](http://www.rssgraffiti.com/ "RSS Graffiti | Feed Your Timeline™") dient dazu, einen RSS-Feed in den eigenen Newsfeed einzubinden.

### Mit Wordpress Newsfeeds aggregieren

Wir haben jetzt schon gesehen, dass man als Wordpress-User automatisch RSS-publiziert. Oft will man aber auch in seinem Blog Inhalte aus anderen Quellen via RSS-integrieren. Ein Beispiel, den Blog-Aggregator des MOOC Maker-Kurs, habe ich schon erwähnt. Diesen Blog-Aggregator habe ich mit dem Plugin [WP RSS Aggregator](http://wordpress.org/extend/plugins/wp-rss-aggregator/ "WordPress › WP RSS Aggregator « WordPress Plugins") realisiert. Ein Problem dieses Plugins— Blogger-Feeds wurden aus unerfindlichen Gründen nicht immer dargestellt—wurde inzwischen behoben. Eine andere Möglichkeit besteht darin, die Headlines der neuesten Posts von Blogs, die man schätzt, anzuzeigen, so wie es [Ingrid Brodnig macht](http://brodnig.org/ "Brodnigs Blog"). Über Plugins dazu informiert [dieses Post](http://smallbusiness.chron.com/make-blogroll-showing-new-blog-entries-wordpress-52354.html "How to Make a Blogroll Showing New Blog Entries on WordPress | Chron.com").

Man kann auch komplette Feeds mit allen Inhalten in ein Blog integrieren, es also als Online-Newsreader benutzen. So etwas wurde bei anderen MOOCs schon praktiziert. Am meisten wird dafür das Plugin [FeedWordPress](http://wordpress.org/extend/plugins/feedwordpress/ "WordPress › FeedWordPress « WordPress Plugins") verwendet. Es schreibt die Posts in dieselbe Datenbanktabelle für die Posts, in der auch die eigenen Posts erscheinen; man kann in den Settings festlegen, dass importierte Posts einer bestimmten Kategorie zugeordnet werden, und die lässt sich wiederum als eigener Bereich des Blogs darstellen. Ich habe selbst FeedWordpress noch nicht benutzt und verlasse mich hier auf [Best RSS Aggregators for WordPress](http://www.wpmayor.com/plugin-reviews/best-rss-aggregators-for-wordpress/ "Best RSS Aggregators for WordPress - WPMayor").

In jedem Fall braucht man Plugins, wenn man auf seinem Blog auch RSS-Feeds aggregieren will. Man findet sie bei der Plugin-Suche unter dem Stichwort [feed](http://wordpress.org/extend/plugins/tags/feed "WordPress › feed « Tags « WordPress Plugins").

### Totgesagte leben länger

RSS wird immer wieder totgesagt. Tatsächlich ist es eine etwas in die Jahre gekommene Technologie, und es ist erklärungsbedürftig—wie es ja auch dieses Post zeigt. Ich muss zugeben, dass ich selbst heute vor allem Twitter für den schnellen Überblick über meine wichtigsten Newsquellen nutze. Ich finde auch die Listen bei Twitter und Facebook nützlich, wobei ich selbst vor allem meine Content Strategy-Liste bei Twitter brauche (die ich auch als eigenen Stream in Flipboard durchblättern kann). Aber Twitter und Facebook bieten mir nur einen Teil der Inhalte, die mich interessieren, und vor allem: Sie sind nicht offen. Sie machen mich von den Entscheidungen großer Unternehmen abhängig. Für eine offene, dezentralisierte Publikations-Infrastruktur braucht man RSS, und wer professionell mit Informationen arbeitet, kommt kaum ohne RSS aus.
