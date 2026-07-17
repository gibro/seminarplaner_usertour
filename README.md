# Seminarplaner – Moodle Nutzertouren (User Tours)

Fertige **Moodle-Nutzertouren** (User Tours) für das
**Seminarplaner**-Plugin, als JSON-Exporte zum Import in eine
Moodle-Installation. Die Touren führen Nutzer:innen Schritt für Schritt
durch die wichtigsten Seiten des Seminarplaners.

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

## Die Touren im Detail

Damit transparent ist, was die Touren zeigen, hier eine Kurzbeschreibung
jeder Tour (Beschreibung jeweils aus der Tour selbst):

### 1. Seminarplaner Überblick — `seminarplaner_ueberblick.json`
*Seite `mod/seminarplaner/grid.php` · 6 Schritte*

Der Überblick zeigt den kompletten Seminarplan als schreibgeschütztes
Zeitraster – zum Betrachten, Veröffentlichen und Exportieren.
Schritte u. a.: Nur-Ansicht-Charakter, Plan wählen und laden,
Veröffentlichen & PDF-Export, Plan im Zeitraster (Farben = Seminarphasen).

### 2. Seminarplaner Sequenz — `seminarplaner_sequenz.json`
*Seite `mod/seminarplaner/sequenz.php` · 18 Schritte*

Einstieg in den neuen Seminarplaner: die Menübereiche und das Bauen des
Ablaufs in der Sequenzansicht. Die umfangreichste Tour (Einstiegs­tour).
Schritte u. a.: alle Menübereiche (Überblick, Sequenz, Bibliothek, Roter
Faden, Import/Export, Einreichen), ersten Seminarplan anlegen, Tage &
Seminarzeiten, didaktische Empfehlungen, als „Roten Faden“
veröffentlichen, automatisches Speichern, Tagesablauf per Drag & Drop,
Farben der Seminarphasen.

### 3. Seminareinheit anlegen — `seminarplaner_seminareinheit.json`
*Seite `mod/seminarplaner/methodlibrary.php?…create=1` · 10 Schritte*

Der Einheiten-Editor: Erklärung der Angaben beim Anlegen oder Bearbeiten
einer Seminareinheit. Schritte u. a.: die drei Abschnitte, Titel
(einziges Pflichtfeld), Lernziele + geführter Lernziel-Helfer, Einordnen
(Seminarphase, Tags, Zeitbedarf, Gruppengröße), alternative Einheiten,
Speichern in die Bibliothek.

### 4. Seminarplaner Bibliothek — `seminarplaner_bibliothek.json`
*Seite `mod/seminarplaner/methodlibrary.php` · 10 Schritte*

Die Bibliothek: Seminareinheiten suchen, neu anlegen, bearbeiten und
stapelweise pflegen. Schritte u. a.: die drei Tabs (lokale Einheiten,
Methodensammlungen, Konzepte), neue Einheit anlegen, bereichsübergreifende
und aktive Suche, Filter (Tags/Phase/Gruppengröße/Zeit), Mehrfachauswahl
für Stapelpflege, Auswählen und Bearbeiten.

### 5. Seminarplaner Einreichen — `seminarplaner_einreichen.json`
*Seite `mod/seminarplaner/review.php` · 7 Schritte*

Einreichen: eigene Seminareinheiten, Methoden-Sammlungen oder ganze
Seminarkonzepte zur Prüfung an die Konzeptverantwortlichen geben.
Schritte u. a.: der Prüf-Ablauf (Einreichen → Prüfung → Freigabe → für
alle da), eigene Einreichungen verfolgen, wer die Konzeptverantwortlichen
sind, die drei Einreich-Wege, Unterschied Sammlung ↔ Konzept.

### 6. Seminarplaner Import/Export — `seminarplaner_import_export.json`
*Seite `mod/seminarplaner/importexport.php` · 9 Schritte*

Import und Export im neuen Layout: zwei Zonen mit je zwei Karten.
Schritte u. a.: Datei-Import (CSV, ZIP, JSON) mit Analyse und Vorschau,
globale Seminarkonzepte übernehmen, Austausch zwischen zwei Planern (JSON),
PDF-Erstellung mit Spaltenwahl und vier Varianten (ZIM-PDF,
Konzeptsammlung, Materialliste, Handout).

### 7. Seminarplaner Einstellungen — `seminarplaner_einstellungen.json`
*Seite `course/modedit.php` (Aktivitätseinstellungen) · 6 Schritte*

Die wenigen Einstellungen einer Seminarplaner-Aktivität: Name, Nutzung
(Beschreibung) und PDF-Logo. Schritte u. a.: Name der Aktivität,
Nutzungsbeschreibung, Logo für die PDF-Exporte, Speichern.

## Hinweise

- Erstellt für das Seminarplaner-Plugin (Entwicklungsstand „umbau").
- Die Tour-Schritte nutzen CSS-Selektoren der Seminarplaner-Oberfläche;
  nach größeren UI-Änderungen des Plugins können einzelne Schritt-Ziele
  angepasst werden müssen.
- Moodle-Dokumentation zu Nutzertouren:
  <https://docs.moodle.org/en/User_tours>
