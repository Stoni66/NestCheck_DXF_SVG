# NestCheck DXF/SVG v2.2.0

**NestCheck DXF/SVG** ist eine Windows-Software fuer die Vorbereitung, Pruefung, Verschachtelung und Ausgabe von DXF- und SVG-Dateien fuer Lasercutter. Die App richtet sich an Maker, Werkstaetten, Laseranwender und kleine Produktionsumgebungen, die mehrere Motive effizient auf Materialplatten platzieren und als laserfertige Dateien exportieren moechten.

Die Version **v2.2.0** enthaelt den aktuellen Importfix fuer SVG-Proportionen. SVG-Motive werden beim Import nicht mehr ungleichmaessig gedehnt, wenn Motivformat und deklarierte SVG-Seitengroesse voneinander abweichen.

## Hauptfunktionen

- Import von SVG- und DXF-Dateien
- Pruefung und Klassifizierung von Konturen
- Mehrteil- und Mehrplatten-Nesting
- schnelles Aussenkontur-Nesting fuer komplexe Dateien
- manuelle Nachbearbeitung platzierter Teile
- Material- und Restmaterialverwaltung
- Speicherung von Restmaterialplatten mit bereits ausgeschnittenen Sperrflaechen
- erneutes Nesting auf gespeicherten Restmaterialplatten
- Export als SVG und DXF
- Maschinenprofile fuer gaengige Lasersysteme
- mehrsprachige Bedienoberflaeche
- integrierte Lizenzierung mit Testphase
- Installer fuer Windows mit Desktop-Verknuepfung und Deinstallation

## Typischer Workflow

1. **Projekt starten**
   - Neues Projekt anlegen oder ein bestehendes Projekt oeffnen.
   - Optional eine Demo laden, um den Ablauf zu testen.

2. **Dateien importieren**
   - SVG- oder DXF-Dateien laden.
   - Stueckzahlen pro Datei festlegen.
   - Die App zeigt Konturen, Hinweise und moegliche Probleme an.

3. **Material einstellen**
   - Plattengroesse definieren, z. B. 600 x 400 mm.
   - Randabstand und Mindestabstand zwischen Teilen einstellen.
   - Optional gespeichertes Restmaterial laden.

4. **Nesting starten**
   - Nestingmodus, Suchschritt, Verdichtung, Winkelraster und weitere Parameter einstellen.
   - Teile werden auf der Materialplatte platziert.
   - Nur echte Aussenkonturen sind fuer das Nesting relevant, damit komplexe Gravur- und Innenlinien das Platzieren nicht unnoetig verlangsamen.

5. **Manuell bearbeiten**
   - Teile bei Bedarf verschieben, drehen, duplizieren oder loeschen.
   - Pfeiltasten erlauben genaue Korrekturen.

6. **Pruefen**
   - Layout auf Kollisionen, Abstaende und Plausibilitaet pruefen.
   - Hinweise und Warnungen koennen vor dem Export kontrolliert werden.

7. **Exportieren**
   - SVG oder DXF fuer die aktuelle Platte oder alle Platten exportieren.
   - Maschinenprofil auswaehlen und Farben sowie Strichstaerken anpassen.

8. **Restmaterial speichern**
   - Nach dem Nesting kann die verbleibende Platte als Restmaterial gespeichert werden.
   - Bereits ausgeschnittene Teile werden als Sperrflaechen gespeichert.
   - Beim naechsten Auftrag kann dieses Restmaterial erneut geladen und weiterverwendet werden.

## Restmaterialverwaltung

Die Restmaterialfunktion ist fuer reale Werkstattablaeufe gedacht. Wird eine Platte teilweise genutzt, kann der verbleibende Bereich als neues Restmaterial gespeichert werden. Dabei merkt sich NestCheck:

- die Aussenkontur der Materialplatte
- alle bereits ausgeschnittenen Teilkonturen
- die dadurch entstandenen Sperrbereiche
- die Materialgroesse und relevanten Parameter

Wenn das Restmaterial spaeter erneut verwendet wird, platziert die App neue Teile nur in noch freien Bereichen. Wird das Restmaterial am Ende nicht mehr benoetigt, kann es verworfen oder geloescht werden.

## Exportprofile

NestCheck unterstuetzt SVG- und DXF-Export fuer verschiedene Lasersysteme. Je nach Maschine koennen Farben und Strichstaerken unterschiedlich interpretiert werden. Deshalb enthaelt die App Exportprofile und einen Exportdialog zur Anpassung.

Typische Profile:

- Trotec / Laser Schnitt
- LightBurn / RDWorks
- Epilog / Universal
- xTool / Generic

Beim SVG-Export koennen unter anderem folgende Linienarten ausgegeben werden:

- Schnitt aussen
- Schnitt innen
- Gravur
- ignorierte Restmaterial- oder Hilfslinien
- offene oder problematische Konturen als Kontrolllayer

## Hinweise zu Laserfarben

Viele Lasersysteme verwenden Farben zur Unterscheidung von Arbeitsschritten. Die Bedeutung der Farben ist jedoch nicht bei allen Herstellern gleich. Deshalb sollten die Exportfarben vor der Produktion immer mit dem verwendeten Lasertreiber oder der Laser-Software verglichen werden.

Bei Trotec-Workflows wird haeufig Rot fuer Schnittkonturen verwendet. Andere Linienfarben koennen z. B. fuer Gravur oder Markierung genutzt werden. NestCheck erlaubt die Anpassung dieser Werte im Exportdialog.

## Installation

1. Die Datei **NestCheck_DXF_SVG_v2_2_0_multilingual_Setup.exe** herunterladen.
2. Den Installer ausfuehren.
3. Den Anweisungen des Setup-Assistenten folgen.
4. NestCheck ueber die Desktop-Verknuepfung oder das Startmenue starten.

Der Installer enthaelt auch ein Deinstallationsprogramm.

## Systemanforderungen

- Windows 10 oder Windows 11
- 64-Bit-System empfohlen
- Bildschirm mit ausreichender Aufloesung fuer technische Layoutvorschau
- Fuer SVG/DXF-Kontrolle wird eine externe Software wie Inkscape, LightBurn oder eine Maschinen-Software empfohlen

## Lizenzierung

NestCheck enthaelt eine Testphase. Nach Ablauf der Testphase ist eine Lizenz erforderlich. Die Lizenzierung arbeitet mit einer Installations-ID. Diese ID kann in der App kopiert und fuer eine Lizenzanfrage verwendet werden.

Die App enthaelt Eingabefelder fuer:

- Name / Firma
- E-Mail-Adresse
- Installations-ID
- Lizenzcode

## Bekannte Hinweise

- Nesting ist bei komplexen Konturen ein mathematisch anspruchsvolles Problem. Sehr komplexe Dateien koennen mehr Rechenzeit benoetigen.
- Die besten Ergebnisse entstehen, wenn die importierten Dateien saubere, geschlossene Aussenkonturen enthalten.
- Innenlinien und Gravuren werden fuer den Export erhalten, sollten aber fuer das eigentliche Nesting nicht als Aussenkontur interpretiert werden.
- Vor der Produktion sollte der Export immer in der Zielsoftware kontrolliert werden.

## Projektstatus

Aktuelle Version: **v2.2.0 multilingual mit SVG-Proportionen-Importfix**

Diese Version ist fuer Windows als Installer vorgesehen und enthaelt die aktuelle NestCheck-Funktionalitaet fuer Import, Pruefung, Nesting, Restmaterial und Export.

## Autor

Designed by **Oswald Steiner**

