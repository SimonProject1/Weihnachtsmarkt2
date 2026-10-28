# Cozy Weihnachtsmarkt-Tripplaner

Statische, installierbare GitHub-Pages-PWA. Lokale Speicherung, flexible Personen, Timeline, Marktfilter, Budget, Haltestellensuche über `v6.db.transport.rest`, Tripplanung und `.ics`-Export.

## GitHub Pages
1. Inhalt dieses Ordners in ein neues Repository hochladen.
2. Repository: **Settings > Pages**.
3. Quelle: **Deploy from a branch**, Branch `main`, Ordner `/ (root)`.
4. Nach dem ersten Online-Aufruf kann die App installiert und offline verwendet werden.

## Lokal testen
Ein lokaler Webserver ist nötig, zum Beispiel:
`python -m http.server 8080`
Danach `http://localhost:8080` öffnen.
