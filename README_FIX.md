# Road to Independence – stabile Live-Version

## Fehlerbehebung
Die vorherige Live-Version hat Presence zu häufig aktualisiert. Supabase begrenzt Presence pro Client.
Diese Version:

- sendet den Presence-Status nur noch etwa alle 15 Sekunden,
- fasst mehrere Spieländerungen zu einem Update zusammen,
- sendet nicht mehr alle 5 Sekunden einen Presence-Track,
- nutzt einen Web Worker für stabilere Realtime-Heartbeats in Hintergrund-Tabs,
- versucht bei Heartbeat-Timeouts automatisch neu zu verbinden.

## Verwendung
Die vorhandene `config.js` bleibt unverändert.

Auf GitHub müssen nur `index.html` und `teacher.html` durch die neuen Versionen ersetzt werden.
`config.js` kann so bleiben.

Nach dem Upload GitHub Pages kurz neu laden. Eventuell den Browser mit Strg+F5 aktualisieren.

## Erwartetes Verhalten
- Schüler erscheinen nach dem Start im Lehrer-Dashboard.
- Fortschritt wird ca. alle 15 Sekunden aktualisiert.
- Ein Schüler bleibt sichtbar, solange sein Spiel geöffnet und mit Realtime verbunden ist.
- Beim Schließen des Spiels verschwindet der Schüler wieder.
