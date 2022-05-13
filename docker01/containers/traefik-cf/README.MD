Die acme.json benötigt chmod 600.
Die Datei nicht öffnen und zur not noch mal neu anlegen wenn es Probleme gibt.

data/config.yml und data/traefik.yml noch anpassen.

Um DASHBOARDUSER & PASS zu generieren folgende Befehle ausführen:

```
apt install apache2-utils
echo $(htpasswd -nb <BENUTZERNAME> <PASSWORT>)
```

Alles zur Wildcard, Cloudflare und Traefik:

https://youtu.be/liV3c9m_OX8


https://techno-tim.github.io/posts/traefik-portainer-ssl/
