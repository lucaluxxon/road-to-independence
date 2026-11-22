# Road to Independence – Live-Sitzung

Diese Variante speichert **keine Schüler-Spielstände dauerhaft**.

## Funktionsweise

- Schüler öffnen `index.html`.
- Sie geben ein Kürzel und einen gemeinsamen Sitzungscode ein.
- Während das Spiel geöffnet ist, sendet der Browser in größeren Abständen nur den aktuellen Live-Status:
  - Kürzel
  - Sitzungscode
  - Fortschritt in %
  - Zahl erledigter Pflichtstationen
  - aktueller Abschnitt
  - aktuelle Spielzeit
- `teacher.html` zeigt alle aktuell verbundenen Schüler desselben Sitzungscodes.
- Wird der Schüler-Tab geschlossen oder die Verbindung getrennt, verschwindet der Live-Eintrag wieder.
- Es gibt keine Datenbanktabelle und keinen wiederherstellbaren Spielstand.
- Ein Neuladen des Schülerspiels setzt den Fortschritt zurück.

## Benötigt

1. kostenloses Supabase-Projekt
2. Project URL
3. Publishable Key (`sb_publishable_...`)
4. öffentliches Hosting, z. B. GitHub Pages

Keine SQL-Befehle, keine Tabellen und keine Supabase-Auth-Konten sind nötig.
