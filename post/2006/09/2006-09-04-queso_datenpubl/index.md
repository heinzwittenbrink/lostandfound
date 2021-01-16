---
title: "Queso --- Datenpublikation via Atom Publishing Protocol"
date: "2006-09-04"
tags: 
  - "syndication"
  - "web-services"
---

Drei junge IBM-Programmierer, Wing Yung, Elias Torres und Ben Szekely, haben als sommer work eine neue experimentelle Anwendung des Atom Publishing Protocols (APP) entwickelt: Queso. (Den Namen inspirierte --- wie bei allen übrigen Komponenten dieser Software --- ein mexikanisches Restaurant gegenüber der Arbeitsstätte der Entwickler.) Queso ist eine J2EE-Anwendung. Sie kombiniert das APP (Version 0.9) mit Technologien des Semantic Web. Dabei werden Ajax-Libraries für das User-Interface und [JSON](http://www.json.org/) für die Datenübergabe an Anwendungen benutzt. Das APP wird für das Web-Frontend eines RDF-Servers (namens Boca) verwendet. Via APP lassen sich die in Boca gespeicherten Daten ergänzen und aktualisieren. Queso greift dabei auf die APP-Implementierung [Abdera](http://incubator.apache.org/abdera/) zurück, ein Inkubator-Projekt der Apache-Foundation.

Um die Atom-Dokumente als RDF-Tripel zu interpretieren, benutzt Queso das von Henry Story entwickelte [Atom in OWL](http://semtext.org/atom/). Queso stellt ein Schnittstelle bereit, um auf die Inhalte des Servers mit der RDF-Abfrage [SPARQL](http://www.w3.org/TR/rdf-sparql-query/) zuzugreifen. Die Queso-Entwickler verwenden also gleich eine ganze Serie von Web 2.0\-Techniken für eine Semantic-Web-Anwendung.

Das APP dient bei Queso dazu, Daten, nicht Texte oder andere Medien, zu publizieren. (Die Entwickler wollen Boca anderen Entwicklern als Repository für Daten und für XHTML/Javascript-Sourcecode anbieten.) Die Atom-Entries repräsentieren Objekte (subjects im Sinne von RDF-Terminologie); die Atom-Elemente des Eintrags werden dabei als Informationen über Eigenschaften dieser Objekte verstanden. Dabei beschränkt sich Queso nicht auf die Metadaten, die das Atom Syndication Format zu Verfügung stellt. Wenn als Inhaltstyp des Dokuments XHTML angegeben ist, geht Boca davon aus, dass es den Regeln von [RDFa](http://www.w3.org/TR/xhtml-rdfa-primer/) folgt. Er wird dann auf dem Server als Serie von Statements über den Gegenstand interpretiert, den der Atom-Eintrag beschreibt. (RDFa ist eine Syntax, die RDF-Inhalte in XHTML verpackt.) Boca konstruiert aus den RDF-Tripeln einen Graphen und verwendet die Atom-Id als Namen für diesen Graphen.

Zugang zu den Daten auf dem Server bietet sowohl ein Atom-Browser wie die SPARQL-Schnittstelle. Atom dient dem Betrachten und Verändern der Daten, SPARQL dem Extrahieren von Informationen.

Der Vorteil der gesamten Anwendung besteht darin, dass Entwickler sehr einfach beliebige und beliebig strukturierte Daten als RDF-Tripel auf Boca ablegen und frei auf sie zugreifen können. Der Zugriff erfolgt dabei standardisiert und flexibel via SPARQL; JSON erlaubt es, die Daten weiterzuverarbeiten, ohne RDF parsen zu müssen. Boca erleichtert es damit, Mashups zu konstruieren, die Daten aus unterschiedlichen Quellen kombinieren.

Queso gehört in den Kontext der durch das Web möglichen Verknüpfungen von heterogenen Daten/Informationen. Auch wer RDF und dem Semantic Web skeptisch gegenübersteht, kann erkennen, dass es die RDF-Tripel-Struktur erleichtert, ganz unterschiedliche Daten aneinander zu binden. Dadurch könnten spontane Mashups wie das --- ebenfalls bei IBM entwickelte --- [QEDwiki](/lostandfound/2006/05/qedwiki.html) leicht realisiert werden.

Eine andere Assoziation: die Präsentationen [The Application of Weblike Design to Data: Designing Data for Reuse](http://www.hackdiary.com/slides/xtech2005/) von Matt Biddulph und [Native to a Web of Data](http://www.plasticbag.org/archives/2006/02/my_future_of_web_apps_slides/) von Tom Coates. Beide kann man als Beschreibungen der Verwendung des Atom Publishing Protocols für die Publikation von Daten verstehen, ohne dass davon explizit die Rede wäre. Es geht in ihnen um ein REST-Interface zu Kollektionen von Daten, wie es von Queso experimentell verwirklicht wird.

\[Quellen: [Elias Torres » Blog Archive » Queso - a Semantic Web/Web 2.0 server](http://torrez.us/archives/2006/07/17/471/);  [~wingerz » Atom/XHTML/RDFa in Queso](http://wingerz.com/blog/?p=35) (Wing Yung); [~wingerz » A Queso Example](http://wingerz.com/blog/?p=38) (Wing Yung); [Into the Woods » Blog Archive » Posting Atom Entries to Queso from Java(tm)](http://www.klinewoods.com/?p=41) (Ben Szekely)\]
