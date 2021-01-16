---
title: "Erfahrungsbericht: Wordpress-Installation mit der Google Compute Engine"
date: "2018-12-02"
categories: 
  - "web"
tags: 
  - "wordpress"
---

Ich habe meine Website—im wesentlichen mein Blog—lange bei [Advania](https://advania.com/ "Advania-Website") laufen lassen. Ursprünglich hatte ich eine virtuelle Maschine bei der isländischen Firma [Greenqloud](https://www.qstack.com/qstack-is-now-powered-by-netapp/ "Artikel zum Kauf von Greenqloud durch Nettapp"). Einerseits bot Greencloud damals einen Betrieb mit grüner Energie an, andererseits war mir ein Provider in Island sympathisch, weil ich zur Not einen Server außerhalb der USA und Europas zur Verfügung haben wollte, und zwar um ausprobieren zu können, wie man Kontrollen beim Publizieren umgehen kann. Greencloud hat das Hosting dann an Advania verkauft, und Advania bietet privaten Einzelnutzern diesen Service jetzt nicht mehr an.

Ich habe keinen Anbieter gefunden, der CO2-neutrales Hosting einer virtuellen Maschine außerhalb der USA oder Europas anbietet. Deshalb habe ich mich bis auf weiteres für Googles Cloud Computing entschieden, weil es ökologisch zu rechtfertigen ist (siehe [Google Cloud und die Umwelt](https://cloud.google.com/environment/)). Möglicherweise werde ich im Laufe des nächsten Jahres wieder wechseln. Physisch befindet sich meine virtuelle Maschine in Amsterdam. Ich gehe davon aus, dass sich Google an die Regeln der DSGVO hält, so dass User nicht befürchten müssen, dass sie getrackt werden. Auf Dauer wäre mir aber eine andere Lösung sympathischer.

Für ein Jahr ist der Service kostenlos, so dass man ihn ohne finanzielles Risiko ausprobieren kann. Was ich nach den ersten Erfahrungen sagen kann: Google macht es einem User leicht, einen virtuellen Server zu installieren. Ich habe trotzdem mehr als 5 Stunden gebraucht, bis mein Blog wieder lief. Ich hoffe jedenfalls, dass alles wieder funktioniert—viel getestet habe ich noch nicht.

Als Betriebssystem für meine virtuelle Maschine verwende ich Debian 9. Den Server laufen zu lassen ging so schnell, dass ich mir keine Notizen dazu gemacht habe. Man klickt bei der [Google Cloud Platform](https://console.cloud.google.com/compute/instancesAdd?project=api-project-784783251126&folder&organizationId "Google Cloud Platform. Konsole") auf _Create Instance_ und wählt aus, was man braucht.

Ich habe dann zuerst einen guten alten LAMP-Server entsprechend [How to Install a LAMP Server on Debian 9 Stretch Linux](https://linuxconfig.org/how-to-install-a-lamp-server-on-debian-9-stretch-linux) installiert. LAMP steht für Linux—Apache—MySQL—PHP und ist die übliche Basis für ein Wordpress-Blog. Bei der Datenbank habe ich entsprechend dieser Anweisung die MariaDB installiert, die komplett unter einer freien Lizenz steht, während MySQL inzwischen Oracle gehört. Die Datenbank-Installation habe ich abgesichert, indem ich

`$ sudo mysql_secure_installation`

eingegeben und die dann folgenden Schritte nachvollzogen habe.

Bei der Wordpress-Installation selbst bin ich nach [How to Install WordPress On Debian 9 Stretch Linux](https://linuxconfig.org/how-to-install-wordpress-on-debian-9-stretch-linux) vorgegangen. Auch das war unproblematisch.

## Migration mit dem Plugin "All-in-One WP Migration"

Nicht ganz so trivial war es, mein Blog zu importieren und das System auf HTTPS umzustellen.

Zur Migration des Blogs habe ich das Plugin [All-in-One WP Migration](https://wordpress.org/plugins/all-in-one-wp-migration/ "Website des Plugins") verwendet. Warum? Weil ich bei der letzten Migration, bei der ich nur die Datenbank exportiert und importiert habe, viel Zeit gebraucht habe, um Thema und Menüs anzupassen. Ich habe das Plugin bei meiner alten und bei meiner neuen Instanz installiert. Das alte Blog in eine Datei zu exportieren und diese downzuloaden war problemlos. Beim Uploaden in das neue Wordpress hatte ich dann aber Schwierigkeiten. Zuerst musste ich das Upload-Limit erhöhen, weil das File mit meinem Blog etwas über 250 MB umfasst. Das ist mir nach etwa Herumprobieren mit den Wordpress bzw. PHP-Konfigurationsfile dank eines [Tipps](https://local.getflywheel.com/community/t/all-in-one-migration-import-limit/4940/5 "All in One Migration Import Limit - WordPress Questions - Local by Flywheel") gelungen:

> In the All-in-one plugin edit the file called constants.php in that file find " max file size " and put a zero at the end of the numbers there this will make the upload size to 5GB

Damit konnte ich die Export-Datei in das neue Blog laden, bekam dann aber Fehlermeldungen bei der Dekompression. Dafür ist offenbar ein Bug in dem Plugin verantwortlich. Es verschwand erst, nachdem ich eine alte Version des Plugins installiert habe, wie es [hier](https://wordpress.org/support/topic/unable-to-open-file-for-reading/ "Topic: Unable to open file for reading | WordPress.org") empfohlen wird.

Durch den Import wird die komplette Datenbank überschrieben. Ich musste über die Kommandozeile wieder einen Administrator-User für mich anlegen, um mich einloggen zu können. (Bei Stack Overflow gefunden: [Hinweis zum Einloggen nach einer Migration mit dem All-in-One WP Migration Plugin](https://stackoverflow.com/questions/50865311/wordpress-cannot-login-after-migrating-with-all-in-one-wp-migration "Cannot login after migrating with All-in-one WP Migration - Stack Overflow").)

## Umstellung auf HTTPS

Das Blog war jetzt unter erreichbar. Der nächste und letzte Schritt war die Umstellung auf HTTPS/bzw. SSL. Damit sorgt man dafür, dass die Kommunikation zwischen dem Browser und dem Server verschlüsselt wird, sie ist damit für Außenstehende nicht mehr lesbar.

Von meiner letzten Installation wusste ich, dass die Umstellung auf HTTPS der problematischste Teil ist. Das war diesmal nicht anders. Der wohl bequemste Weg ist, mithilfe des Programms [Certbot](https://certbot.eff.org/ "Automatically enable HTTPS on your website with EFF's Certbot, deploying Let's Encrypt certificates.") ein Zertifikat von [Let's Encrypt](https://letsencrypt.org/ "Let's Encrypt - Free SSL/TLS Certificates") zu beziehen. Bei Debian 9 kann man Certbot aus den offiziellen Paketen installieren. Ich bin nach [dieser Anweisung zum Installieren von Certbot bei Debian 9](https://certbot.eff.org/lets-encrypt/debianstretch-apache.html "Certbot - Debianstretch Apache") vorgegangen, das war völlig unproblematisch. Allerdings konnte ich danach keine Blogposts mehr aufrufen (wohl aber Bilder). Ich muss zugeben, dass ich nicht genau verstanden habe, worin die Ursache liegt. Nach einigem Herumprobieren habe ich das Plugin [Really Simple SSL](https://really-simple-ssl.com/) installiert, bin aber nicht sicher, ob das eine Wirkung hatte. Es ändert die Datei .htaccess zu

```
# BEGIN rlrssslReallySimpleSSL rsssl_version[3.1.2]
<ifmodule mod_rewrite.c="">
RewriteEngine on
RewriteCond %{HTTPS} !=on [NC]
RewriteRule ^(.*)$ https://%{HTTP_HOST}/$1 [R=301,L]
</ifmodule>
# END rlrssslReallySimpleSSL
# BEGIN WordPress
<ifmodule mod_rewrite.c="">
RewriteEngine On
RewriteBase /lostandfound/
RewriteRule ^index\.php$ - [L]
RewriteCond %{REQUEST_FILENAME} !-f
RewriteCond %{REQUEST_FILENAME} !-d
RewriteRule . /lostandfound/index.php [L]
</ifmodule>
# END WordPress
```

Genau dasselbe hatte ich allerdings schon vorher eingetragen. Blogposts ließen sich weiter nicht aufrufen. Sie waren erst erreichbar, nachdem ich in `/etc/apache2/sites-available/000-default-le-ssl.conf` innerhalb von `<virtualhost *:443="">` hinzugefügt hatte

```
<directory var="" www="">
Options Indexes FollowSymLinks MultiViews
# changed from None to FileInfo
AllowOverride FileInfo
Order allow,deny
allow from all
</directory>
RewriteEngine on
```

(Entsprechend [\[SOLVED\] Redirect Error: Wordpress + Let's Encrypt (Certbot) + SSL only + non-www - Server - Let's Encrypt Community Support](https://community.letsencrypt.org/t/solved-redirect-error-wordpress-lets-encrypt-certbot-ssl-only-non-www/20865 "[SOLVED] Redirect Error: Wordpress + Let's Encrypt (Certbot) + SSL only + non-www - Server - Let's Encrypt Community Support").)

Danach funktionierte alles bis auf eine Fehlermeldung des Plugins [Avatar Privacy | WordPress.org](https://wordpress.org/plugins/avatar-privacy/ "Avatar Privacy | WordPress.org"). Es verlangt das PHP-Modul gd, dass ich mit

```
$ sudo apt install php-curl php-gd php-mbstring
php-xml php-xmlrpc php-soap php-intl php-zip

$ sudo systemctl restart apache2

```

installiert habe. (entsprechend [Install Wordpress on LAMP in Debian 9](https://www.howtoforge.com/tutorial/install-wordpress-on-lamp-in-debian-9/ "Install Wordpress on LAMP in Debian 9")). Ein erster Versuch mit `sudo apt-get install php7.0-gd` führte dazu, dass Wordpress nicht mehr funktionierte, sodass ich php7.0-gd wieder deinstalliert habe.)

* * *

Mich stressen solche Installationen, und deshalb notiere ich mir oft zu wenig. Aber ich freue mich, wenn ich es geschafft habe—das ist etwas wie beim Kochen. Ich habe mein eigenes Publikationsinstrument wenigstens halbwegs unter Kontrolle.
