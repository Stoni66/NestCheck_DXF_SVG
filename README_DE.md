# NestCheck DXF/SVG v2.5.0

**NestCheck DXF/SVG** ist eine Windows-Software zum Importieren, Pruefen, Nesten und Exportieren von SVG- und DXF-Dateien fuer Lasercutter. Die App ist fuer Maker, Werkstaetten, Laseranwender und kleine Produktionsumgebungen gedacht, die mehrere Schnitt- und Gravurmotive sauber auf Materialplatten oder Restmaterial platzieren moechten.

Version **v2.5.0** erweitert NestCheck um eine deutlich bessere Verarbeitung von Motiven mit **Gravurbild plus schneidbarer Aussenkontur**. Damit koennen Dateien aus LaserCut KonturFix v2.5.0 mit eingebetteter Rastergravur, rotem Schneidrahmen und weiteren Schnittlinien importiert, genestet und wieder exportiert werden.

## Download

Aktueller Windows-Installer:

[**NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe herunterladen**](https://github.com/Stoni66/NestCheck_DXF_SVG/releases/download/v2_5_0/NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe)

Release-Tag: **v2_5_0**

## Was ist neu in v2.5.0?

- Unterstuetzung fuer SVG-Dateien mit eingebetteten Rastergravuren
- Gravurbild und schneidbare Aussenkontur bleiben beim Nesten deckungsgleich
- Gemeinsame Transformation fuer Konturen und eingebettete Bilder beim Platzieren, Drehen und Exportieren
- Verbesserte Vorschau fuer Gravurdateien mit Rahmen
- Aktualisierte Hilfe und Quickinfos
- Durchgehend ueberarbeitete Bedienoberflaeche fuer v2.5.0
- Nuitka-basierter Windows-Build fuer besseren Quellcodeschutz gegen einfaches Auslesen
- Mehrsprachige Oberflaeche mit gespeicherter Spracheinstellung

## Hauptfunktionen

- Import von SVG- und DXF-Dateien
- Import von SVG-Dateien mit eingebetteten Rasterbildern fuer Gravur
- Klassifizierung von Schnitt aussen, Schnitt innen, Gravur, offenen Linien, ignorierten Linien und Problemkonturen
- Mehrteil- und Mehrplatten-Nesting
- Aussenkontur-Nesting fuer komplexe Dateien
- Rotation in einstellbaren Winkelrastern
- manuelle Nachbearbeitung platzierter Teile
- Materialverwaltung mit Plattengroesse, Randabstand und Mindestabstand
- Restmaterialverwaltung mit bereits ausgeschnittenen Sperrflaechen
- erneutes Nesten auf gespeicherten Restmaterialplatten
- SVG- und DXF-Export fuer aktuelle Platte oder alle Platten
- Maschinenprofile fuer Trotec, LightBurn/RDWorks, Epilog/Universal und xTool/Generic
- Exportdialog fuer Farben und Strichstaerken
- integrierte Testphase und Lizenzaktivierung
- Windows-Installer mit Desktop-Verknuepfung und Deinstallation

## Typischer Workflow

1. **Projekt starten**
   - Neues Projekt anlegen oder ein bestehendes Projekt oeffnen.
   - Optional eine Demo laden, um den Ablauf zu testen.

2. **SVG/DXF importieren**
   - Eine oder mehrere SVG- oder DXF-Dateien laden.
   - Stueckzahlen festlegen.
   - Konturen und Hinweise pruefen.

3. **Material festlegen**
   - Plattengroesse einstellen, z. B. 600 x 400 mm.
   - Randabstand und Mindestabstand definieren.
   - Optional eine gespeicherte Restmaterialplatte laden.

4. **Nesting starten**
   - Nestingmodus, Suchschritt, Winkel, Verdichtung und weitere Parameter einstellen.
   - Die App platziert die Teile auf der Platte.
   - Fuer das eigentliche Nesting zaehlt vor allem die echte Aussenkontur. Innenlinien und Gravurbilder werden fuer die Ausgabe erhalten.

5. **Manuell korrigieren**
   - Platzierte Teile koennen verschoben, gedreht, dupliziert oder geloescht werden.
   - Bei Gravurmotiven mit Rahmen werden Bild und Rahmen gemeinsam bewegt.

6. **Layout pruefen**
   - Layout auf Kollisionen, Abstaende und Plausibilitaet pruefen.
   - Warnungen und Hinweise kontrollieren.

7. **Exportieren**
   - Passendes Maschinenprofil auswaehlen.
   - SVG oder DXF fuer aktuelle Platte oder alle Platten exportieren.
   - Farben und Strichstaerken bei Bedarf vor dem Export anpassen.

8. **Restmaterial speichern**
   - Nach dem Nesting kann die verbleibende Platte als Restmaterial gespeichert werden.
   - Bereits ausgeschnittene Aussenkonturen werden als Sperrflaechen gespeichert.
   - Beim naechsten Auftrag kann dieses Restmaterial erneut verwendet werden.

## Gravur mit schneidbarem Rahmen

NestCheck v2.5.0 kann SVG-Dateien verarbeiten, bei denen ein detailreiches Gravurbild als eingebettetes Rasterbild enthalten ist und zusaetzlich eine schneidbare Aussenkontur vorhanden ist. Das ist besonders nuetzlich fuer Motive, die in LaserCut KonturFix im Modus **Gravur + Aussenkontur** erstellt wurden.

Wichtig:

- Die rote Aussenkontur dient als Schnittkontur und bestimmt die Nestingform.
- Das eingebettete Gravurbild bleibt optisch erhalten.
- Beim Nesten und Exportieren werden Bild und Aussenkontur gemeinsam verschoben und gedreht.
- In Inkscape oder der Lasersoftware sollte der Export vor der Produktion kontrolliert werden.

## Restmaterialverwaltung

Die Restmaterialfunktion ist fuer reale Werkstattablaeufe gedacht. Wird eine Platte teilweise genutzt, kann der verbleibende Bereich gespeichert werden. NestCheck merkt sich dabei:

- Materialgroesse
- Aussenkontur der Platte
- bereits ausgeschnittene Teilkonturen
- dadurch blockierte Bereiche
- relevante Materialparameter

Beim spaeteren Laden des Restmaterials werden neue Teile nur in freien Bereichen platziert. Wenn ein Restmaterial nicht mehr sinnvoll nutzbar ist, kann es geloescht oder verworfen werden.

## Exportprofile und Laserfarben

Viele Lasersysteme interpretieren Farben und Strichstaerken als Arbeitsbefehle. NestCheck enthaelt deshalb verschiedene Maschinenprofile und erlaubt das Anpassen der Ausgabe.

Typische Zuordnung:

- **Rot**: Schnitt aussen
- **Gruen**: Schnitt innen
- **Blau**: Gravur
- **Grau**: ignorierte Restmaterial- oder Hilfslinien
- **Orange/Magenta**: offene oder problematische Kontrolllinien

Die genaue Bedeutung kann je nach Maschine und Software unterschiedlich sein. Vor der Produktion sollte die Datei immer in der Zielsoftware geprueft werden.

## Installation

1. Installer herunterladen: `NestCheck_DXF_SVG_v2_5_0_nuitka_multilingual_Setup.exe`
2. Datei starten.
3. Den Schritten des Setup-Assistenten folgen.
4. NestCheck ueber Desktop-Verknuepfung oder Startmenue starten.

Der Installer enthaelt auch ein Deinstallationsprogramm.

## Systemanforderungen

- Windows 10 oder Windows 11
- 64-Bit-System empfohlen
- Ausreichende Bildschirmaufloesung fuer die Layoutvorschau
- Optional: Inkscape, LightBurn, RDWorks oder eine maschinenspezifische Lasersoftware zur Kontrolle der Exporte

## Lizenzierung

NestCheck enthaelt eine Testphase. Danach ist eine Lizenz erforderlich. Die Lizenzierung arbeitet mit einer Installations-ID, die in der App angezeigt und fuer eine Lizenzanfrage verwendet werden kann.

Die App enthaelt Felder fuer:

- Name / Firma
- E-Mail-Adresse
- Installations-ID
- Lizenzcode

## Hinweise fuer beste Ergebnisse

- Saubere, geschlossene Aussenkonturen verbessern das Nesting deutlich.
- Gravurdetails sollten nicht als Aussenkontur interpretiert werden.
- Bei komplexen Motiven ist der Aussenkontur-Modus meist schneller und stabiler.
- Exportierte Dateien immer vor der Produktion in der Zielsoftware kontrollieren.
- Bei Restmaterialplatten darauf achten, dass alte Ausschnitte korrekt als Sperrflaechen angezeigt werden.

## Projektstatus

Aktuelle Version: **NestCheck DXF/SVG v2.5.0 multilingual Nuitka**

Diese Version ist fuer Windows als Installer vorgesehen und enthaelt die aktuelle Funktionalitaet fuer Import, Pruefung, Nesting, Restmaterial, Gravur-mit-Rahmen-Verarbeitung und laserfertigen Export.

## Autor

Designed by **Oswald Steiner**
