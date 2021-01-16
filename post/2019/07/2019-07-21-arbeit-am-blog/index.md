---
title: "Arbeit am Blog"
date: "2019-07-21"
categories: 
  - "journal"
tags: 
  - "blogging"
---

Ich versuche, mein Blog und meine Website zu überarbeiten—unter anderem auch, damit die [IndieWeb](https://indieweb.org/)\-Features bei mir funktionieren. Gestern habe ich die Site endlich so umgestellt, dass auch die Startseite von Wordpress generiert wird, mein Blog aber weiter in einem eigenen Verzeichnis läuft. Ich kann mich jetzt mit der URL [https://wittenbrink.net](https://wittenbrink.net) und über meine Website auf Sites authentifizieren, die das [OAuth](https://oauth.net/)\-Protokoll unterstützen. Ich habe es unter anderem bei [IndieAuth](https://indieauth.com/) getestet. Auf meiner Website funktioniert das mithilfe des [IndieAuth](https://wordpress.org/plugins/indieauth/)\-Plugins.

Nur zur Dokumentation für mich selbst–sorry, wenn das kryptisch ist:

Um sicherzustellen, dass Wordpress in einem eigenen Verzeichnis läuft, aber trotzdem die Startseite von Wordpress generiert wird, habe ich mich an [Giving WordPress Its Own Directory](https://wordpress.org/support/article/giving-wordpress-its-own-directory/) gehalten.

Den korrekten-String (`SetEnvIf Authorization "(.*)" HTTP_AUTHORIZATION=$1`) für meine `.htaccess`\-Datei habe ich [hier](https://devhacksandgoodies.wordpress.com/2014/06/27/apache-pass-authorization-header-to-phps-_serverhttp_authorization/) gefunden. Vorher habe ich vom IndieAuth-Plugin nur Fehlermeldungen bekommen.
