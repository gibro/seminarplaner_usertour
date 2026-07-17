# Seminarplaner – Moodle Nutzertouren (User Tours)

Fertige **Moodle-Nutzertouren** (User Tours) für das
**Seminarplaner**-Plugin, als JSON-Exporte zum Import in eine
Moodle-Installation. Die Touren führen Nutzer:innen Schritt für Schritt
durch die wichtigsten Seiten des Seminarplaners.

## Enthaltene Touren

| Datei | Tour | Gilt auf Seite | Schritte |
|---|---|---|---|
| `seminarplaner_ueberblick.json` | Seminarplaner Überblick | Kursraster – `mod/seminarplaner/grid.php` | 6 |
| `seminarplaner_sequenz.json` | Seminarplaner Sequenz | Sequenzansicht – `mod/seminarplaner/sequenz.php` | 18 |
| `seminarplaner_seminareinheit.json` | Seminareinheit anlegen | Methodenbibliothek (Neu) – `methodlibrary.php?…create=1` | 10 |
| `seminarplaner_bibliothek.json` | Seminarplaner Bibliothek | Methodenbibliothek – `mod/seminarplaner/methodlibrary.php` | 10 |
| `seminarplaner_einreichen.json` | Seminarplaner Einreichen | Review/Einreichen – `mod/seminarplaner/review.php` | 7 |
| `seminarplaner_import_export.json` | Import/Export | `mod/seminarplaner/importexport.php` | 9 |
| `seminarplaner_einstellungen.json` | Einstellungen | Aktivitätseinstellungen – `course/modedit.php` | 6 |

## Import in Moodle

Die Touren werden **als Administrator:in** importiert:

1. In Moodle mit Administrationsrechten anmelden.
2. **Website-Administration → Darstellung → Nutzertouren** öffnen –
   oder direkt die URL aufrufen:

   ```
   https://DEINE-MOODLE-URL/admin/tool/usertours/configure.php
   ```

   (z. B. `https://moodle.example.org/admin/tool/usertours/configure.php`)
3. Auf **„Tour importieren"** klicken.
4. Die gewünschte `*.json`-Datei aus diesem Repository auswählen und
   hochladen.
5. Die Tour erscheint danach in der Liste. Bei Bedarf über das
   **Auge-Symbol aktivieren** (importierte Touren sind ggf. zunächst
   deaktiviert) und Reihenfolge/Einstellungen anpassen.

Für jede der JSON-Dateien wiederholen, die du bereitstellen möchtest.

Jede Tour ist über ihr **URL-Muster (pathmatch)** an die passende
Seminarplaner-Seite gebunden (siehe Tabelle) und wird dort automatisch
angeboten.

## Hinweise

- Erstellt für das Seminarplaner-Plugin (Entwicklungsstand „umbau").
- Die Tour-Schritte nutzen CSS-Selektoren der Seminarplaner-Oberfläche;
  nach größeren UI-Änderungen des Plugins können einzelne Schritt-Ziele
  angepasst werden müssen.
- Moodle-Dokumentation zu Nutzertouren:
  <https://docs.moodle.org/en/User_tours>
