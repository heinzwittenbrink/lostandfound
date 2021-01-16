---
title: "Von Wordpress zu Ghost–Protokoll der Migration"
date: "2015-10-04"
categories: 
  - "web"
tags: 
  - "ghost"
  - "wordpress"
---

In den vergangenen Tagen habe ich das Content Management-System dieses Blogs gewechselt. Ich bin von dem bewährten [WordPress](https://de.wordpress.org/ "WordPress › Deutsch") auf das neue [Ghost](https://ghost.org/ "Ghost - Just a blogging platform") umgestiegen, selbstgehostet auf einem neu eingerichteten Server. Ich habe gelesen, dass Ghost-User traditionell in einem ersten Post beschreiben, wie sie das System eingerichtet haben. Ich schließe mich hier an—wobei allerdings die Migration von Wordpress zu Ghost aufwändiger war als das Einrichten von Ghost selbst. Ich hätte das Ganze ohne die intensive Hilfe meines geduldigen Sohns [David](https://twitter.com/d_wittenbrink "David Wittenbrink (@D_Wittenbrink) | Twitter") nicht geschafft. Er hat mich auch dazu gebracht, Ghost auszuprobieren. Ich möchte es als Beispiel für ein modernes, auf Node.js basierendes CMS kennenlernen.

Dieses Post ist für viele sicher kryptisch. Ich schaffe es jetzt nicht, die Details ausführlich zu erklären. Ich hoffe, die Beschreibung nützt Leuten, die selbst zu Ghost übergehen.

### Server

Mein neuer Server ist eine virtuelle Instanz bei den [Advania Cloud Services](http://www.advania.com/datacentres/solutions/advania-cloud-services/ "Advania Cloud Services"). Fürs Erste benutze ich eine billige Micro Lead-Instanz mit 512 MB RAM.

### Betriebssystem

Ich habe mich als Betriebssystem wieder für Debian entschieden, weil ich es besser kenne als andere Versionen und weil es sich um ein komplettes Open Source-System handelt. Dabei habe ich die von Advania angebotene Version 8.1 genommen.

### Node.js und Ghost installieren

Für die Installation von Ghost habe ich mich an [Installing ghost on an EC2 Debian Jessie instance running nginx](http://blog.timday.com/live-on-ec2/ "Installing ghost on an EC2 Debian Jessie instance running nginx") orientiert, weil mir das Vorgehen simpel erschien und weil die Advania-Instanzen mit Amazon EC2 kompatibel sind. Dabei werden node.js und Ghost im Verzeichnis von `root` installiert—das ist wahrscheinlich in vielen Fällen keine gute Lösung. Sie hat jedenfalls sofort funktioniert. Die Konfigurationsdatei von Ghost `root/node_modules/ghost/config.js` beginnt bei mir:

```
config = {
    // ### Production
    // When running Ghost in the wild, use the production environment.
    // Configure your URL and mail settings here
    production: {
        url: 'http://wittenbrink.net/lostandfound/',
        mail: {},
        database: {
            client: 'sqlite3',
            connection: {
                filename: path.join(__dirname, '/content/data/ghost.db')
            },
            debug: false
        },
        server: {
            host: '127.0.0.1',
            port: '2368'
        }
    },
```

### Verbindung von Ghost mit Nginx

Viel aufwändiger war es dann, Ghost mit Nginx zu verbinden, den ich als Webserver benutze. Wie bei Ghost geht es mir darum, Nginx kennenzulernen. Meine Konfiguration sieht so aus:

```
server {
    listen       80;
    server_name  www.wittenbrink.net;
    return       301 http://wittenbrink.net$request_uri;
}
server {
    listen       80;
    server_name  wittenbrink.net;
location / {
      rewrite ^/$ http://wittenbrink.net/lostandfound permanent;
    }
        location ~* /lostandfound {
        rewrite "lostandfound/[0-9]{4}/[0-9]{2}/(.*)$" /lostandfound/$1 permanent;
        proxy_set_header X-Real-IP $remote_addr;
        proxy_set_header Host $http_host;
        proxy_pass http://127.0.0.1:2368;
   }
 }
```

Zu Anfang werden Anfragen an `www.wittenbrink.net`an `wittenbrink.net`umgeleitet. Die `rewrite`\-Regel hinter `location` sorgt dafür, dass Anfragen an die Domain `wittenbrink.net` gleich an mein Blog unter `http://wittenbrink.net/lostandfound` weitergegeben werden. Im Block darunter gibt es vier Regeln, von denen die letzten drei von [Running Ghost in a Subdirectory with a Static Nginx Site](http://jonathonstaff.com/blog/running-ghost-in-a-subdirectory-with-a-static-nginx-site/ "Running Ghost in a Subdirectory with a Static Nginx Site") übernommen sind. Sie leiten Anfragen an mein Blog an Ghost weiter, das auf dem Port 2368 läuft. Die `rewrite`\-Regel hinter `location ~* /lostandfound` sorgt mit einem regulären Ausdruck dafür, dass Anfragen an die alten URLs von Posts, die die Jahreszahl und den Monat enthielten, auf die neuen URLs umgeleitet werden, in denen der Titel des Posts direkt auf die URL des Blogs folgt. Links auf die Posts funktionieren also weiter. Das `lostandfound` wird in dieser Regel wiederholt, weil Ghost für Bilder auch URLs mit Jahres- und Monatszahlen verwendet. Sie würden sonst herausgefiltert.

### Einrichten von Supervisor für den automatischen Start

Um Ghost nicht nach jedem Systemstart manuell starten zu müssen, habe ich [Supervisor](http://supervisord.org/ "Supervisor: A Process Control System — Supervisor 3.1.3 documentation") installiert. Das Konfigurationsskript `etc/supervisor/conf.d/ghost`:

```
[program:ghost]
command = node /root/node_modules/ghost/index.js
directory = /root/node_modules/ghost
user = root
autostart = true
autorestart = true
stdout_logfile = /var/log/supervisor/ghost.log
stderr_logfile = /var/log/supervisor/ghost_err.log
environment = NODE_ENV="production"
```

Ich bin erst nach einem leichten Verzweiflungsanfall darauf gekommen, dass man in der letzten Zeile `production` einfügen muss, wenn man will, dass Ghost nach einem Neustart das eigene Blog und nicht eine jungfräuliche Version zeigt. Standardmäßig startet Ghost im Entwicklungsmodus mit einer fast leeren Datenbank.

### Migration der Wordpress-Daten

Für die Migration der Blogposts haben wir uns an [Migrating WordPress to Ghost](https://www.ghostforbeginners.com/how-to-transfer-blog-posts-from-wordpress-to-ghost/ "Migrating WordPress to Ghost") gehalten. Allerdings sind die Bilder noch nicht übernommen; ich möchte sie auf einem anderen Server, vermutlich bei [SmugMug](https://www.smugmug.com/ "Photo Sharing. Stunning Photo Websites. | SmugMug") hosten. Der Import hat mehrfach nicht funktioniert, ohne dass eine spezifische Fehlermeldung gekommen wäre. Wir sind dann darauf gekommen, dass Nginx so voreingestellt ist, dass nur Dateien bis 1MB Größe hochgeladen werden können. Nachdem wir in `etc/nginx/nginxconf` hinzugefügt hatten:

```
        client_max_body_size 20m;
```

hat der Upload problemlos funktioniert.

### Kommentare und Disqus

Die Kommentare ließen sich relativ leicht mit den [Migrationstools von Disqus](https://help.disqus.com/customer/portal/articles/286778-migration-tools "Migration Tools | DISQUS") migrieren. Dabei haben wir erst die komplette Wordpress-Datenbank von einem lokal mit [MAMP](https://www.mamp.info/de/ "MAMP & MAMP PRO") installierten Wordpress in Disqus importiert und dann mithilfe des URL-Mappers —sprich: einer [CSV](https://www.google.at/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=CSV "CSV - Google-Suche")\-Datei mit den alten und den neuen URLs— den Posts im Ghost-Blog zugeordnet.

### Todos:

In der neuen Version des Blogs fehlen, wie erwähnt, die Bilder noch. Außerdem enthalten eine Reihe Posts [Markdown](https://daringfireball.net/projects/markdown/ "Daring Fireball: Markdown")\-Texte, wohl weil ich lange mit einem Plugin geschrieben habe, das dafür sorgt, dass die Texte in Markdown gespeichert werden. **Update, 5.10.2015:** Ich hatte vergessen, Anfragen an `www.wittenbrink.net`an `wittenbrink.net`umzuleiten. Das habe ich jetzt getan, zur Erklärung siehe [redirect - Nginx no-www to www and www to no-www - Stack Overflow](http://stackoverflow.com/questions/7947030/nginx-no-www-to-www-and-www-to-no-www "redirect - Nginx no-www to www and www to no-www - Stack Overflow"). Danke an [Ursula Kronenberger](http://www.living-crossmedia.de "Living Crossmedia, die Agentur Ursula Kronenbergers") für den Hinweis auf das Versäumnis!
