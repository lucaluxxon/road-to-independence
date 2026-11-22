# Einrichtung der Live-Version

## 1. Supabase-Projekt anlegen
Ein neues Supabase-Projekt erstellen.

## 2. Public Realtime Channels prüfen
Im Supabase-Dashboard unter den Realtime-Einstellungen muss öffentlicher Zugriff auf Channels erlaubt sein.
Für diese Unterrichtsversion wird Realtime Presence verwendet; keine Datenbanktabelle ist nötig.

## 3. URL und Publishable Key kopieren
Im Connect-Dialog des Projekts:
- Project URL
- Publishable Key (`sb_publishable_...`)

Keinen Secret Key verwenden.

## 4. config.js bearbeiten
Die beiden Platzhalter ersetzen:

window.ROAD_CONFIG = {
  SUPABASE_URL: "https://....supabase.co",
  SUPABASE_PUBLISHABLE_KEY: "sb_publishable_..."
};

## 5. Dateien veröffentlichen
`index.html`, `teacher.html` und `config.js` gemeinsam auf GitHub Pages oder einem anderen statischen Hoster veröffentlichen.

## 6. Unterricht starten
Lehrer:
1. `teacher.html` öffnen.
2. Einen nur für diese Stunde verwendeten Sitzungscode wählen, z. B. `8b-1911`.
3. Auf „Live verbinden“ klicken.
4. Sitzungscode an die Klasse geben.

Schüler:
1. `index.html` öffnen.
2. Kürzel eingeben.
3. exakt denselben Sitzungscode eingeben.
4. Spiel starten.

## Datenschutz / Verhalten
Die Anwendung legt selbst keine Schülerdaten in Tabellen oder im Browser-Speicher ab.
Realtime Presence hält den Status nur während der aktiven Verbindung im Channel.
Nach Schließen der Verbindung ist kein Spielstand zum späteren Wiederaufrufen vorhanden.

Hinweis: Der Publishable Key ist Browser-Code und deshalb öffentlich sichtbar. Niemals einen Secret Key in `config.js` eintragen.
