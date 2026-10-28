# Cozy Weihnachtsmarkt-Tripplaner V2.0.0

Statische, installierbare GitHub-Pages-PWA für Weihnachtsmarkt-Trips ab Wuppertal.

## Enthalten

- 39 Märkte insgesamt, davon 30 neu recherchierte Ziele
- Marktquellen und Prüfdatum direkt in den Details
- Filter nach Stadt, ungefährer ÖPNV-Fahrzeit, Luftlinie, Öffnungstag und Wunschmerkmal
- Sortierung nach Empfehlung, Fahrzeit, Distanz, Stadt oder Startdatum
- Favoriten, lokale Speicherung, Datensicherung und Import
- Timeline mit beliebig vielen Personen und gemeinsamen freien Tagen
- Tripplanung mit Budget, Aktivität, Notizen und gespeicherter Zielhaltestelle
- DB-basierte Haltestellensuche über `v6.db.transport.rest`
- `.ics`-Export mit Zeitzone Europe/Berlin
- installierbare Offline-PWA mit relativem GitHub-Pages-Pfad
- cozy, mobile Oberfläche mit unterer Navigation auf Smartphones

## GitHub Pages

1. Den **Inhalt** dieses Ordners in die oberste Ebene eines neuen GitHub-Repositorys hochladen.
2. In GitHub **Settings → Pages** öffnen.
3. **Deploy from a branch**, Branch **main**, Ordner **/(root)** wählen.
4. Die veröffentlichte Seite einmal online öffnen. Danach stehen App und Marktdaten offline bereit.

## Lokal starten

```bash
python3 -m http.server 8080
```

Danach `http://localhost:8080` öffnen. Ein Webserver ist nötig; ein Doppelklick auf `index.html` reicht für PWA und Offline-Cache nicht aus.

## Tests

```bash
node tests/smoke.mjs
```

Die Tests prüfen unter anderem:

- 39 eindeutige Märkte und genau 30 neue Ziele
- Pflichtfelder, Termine, Quellen, Budget, Fahrzeit und Distanz
- Datumslogik, Sonder-Schließtage und einzelne Wochenendmärkte
- Timeline-/Personenmigration ohne Namenskollision
- `.ics`-Escaping, Zeitzone und Zeilenfaltung
- Manifest, Offline-Dateien und Ausschluss der DB-API aus dem Cache

## Datenhinweis

Markttermine und offizielle Quellen wurden am 28.10.2026 geprüft. Die Quellen sind in den Marktdetails verlinkt. Fahrzeiten sind gerundete Planwerte ab Wuppertal Hbf; Distanzen sind ungefähre Luftlinien. Verbindung, Sonderfahrplan und Marktseite bitte kurz vor der Abfahrt erneut prüfen.
