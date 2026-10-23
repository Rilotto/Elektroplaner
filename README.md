# Elektroplaner

Planungshilfe für die Elektro-Neuinstallation eines Hauses, optimiert für Tablets. Ableger des [Raumplaners](https://github.com/Rilotto/Raumplaner).

## Nutzen
Seite in Chrome öffnen → Menü → „Zum Startbildschirm hinzufügen“. Danach startet der Planer wie eine App und funktioniert auch offline.

## Stand: Phase 1 – Grundriss und Etagen
- Etagen frei anlegen, umbenennen, sortieren, mit Höhenlage, Raumhöhe und Deckenstärke; Hauptverteiler-Etage wählbar
- Wände als Bauteile mit Dicke, Wandtyp und Bauart (Vorlagen in den Einstellungen, frei erweiterbar, Hohlwand ja/nein)
- Wände zeichnen per Antippen oder mit Maß und Richtung, Raum aus Innenmaßen anlegen
- Räume entstehen automatisch aus den Wänden, Innenfläche und Umfang werden berechnet
- Status je Wand und Öffnung: Bestand bleibt / entfällt / neu; Ansichten Ist, Soll und Umbau
- Türen, Fenster, Durchgänge; Maße wahlweise innen oder als Rohbaumaß außen
- Etage darunter als Unterlage, Maßband, Rückgängig, Export als Bild und PDF

## Stand: Phase 2 – Elemente
- Ebene „Elektro“ mit Katalog: Steckdosen, Schalter, Taster, Leuchten, Außen (inkl. Vorlage Hauseingang), Klingel, Netzwerk, Verteiler, Rauchwarnmelder u. a.
- Schaltzeichen in Anlehnung an DIN EN 60617, Wanddosen rasten an der Wandseite ein und wandern mit der Wand
- Status bleibt/entfällt/neu, Montagehöhe (Standardhöhen in den Einstellungen), Montageart nach Bauart, Fachzahl
- Schalter ordnen ihre Leuchten und schaltbaren Steckdosen zu; Wechsel- und Kreuzschaltungen entstehen aus mehreren Schaltstellen
- Verbindungen immer im Plan, rechtwinklig entlang der Wände, farbig nach Leitungsart
- Schaltbild je Schaltung mit Klemmen und Aderfarben, verdrahtet in den Schalterdosen ohne Abzweigdosen
- Reiter für Elemente, Schaltungen, Legende und Etagen-Übersicht; Varianten je Etage

## Stand: Phase 3 – Verteiler und Stromkreise
- Stromkreise mit Nummer, Bezeichnung, Farbe, Verteiler, Schutzorgan, FI/RCD und Leitung; Prüfhinweise zu FI-Pflicht, Querschnitt und Absicherung
- Zuordnen per Antippen im Plan, ganze Schaltungen gemeinsam; Schnellaktionen je Raum für Steckdosen, Licht und eigene Geräte
- Ebene „Verteiler“: Vorderansicht mit Reihen und TE, Leitungsschutzschalter unter ihrem FI, Belegt/Frei, Geräte frei ergänzbar
- Zuleitungen der Unterverteiler mit Absicherung im versorgenden Verteiler
- Stromkreisliste für alle Etagen, Export als CSV, Belegung als Bild

## Stand: Phase 4 – Leitungen und Mengen
- Leitungswege je Stromkreis automatisch: im Raum entlang der Wände in der gewählten Zone, Raum- und Etagenwechsel markiert
- Länge je Stromkreis und Leitungstyp: Weg + senkrechte Stücke zur Zone + Etagenwechsel + Reserve je Anschluss + Verschnitt
- Senkrechte Installationszonen nach DIN 18015-3 einblendbar
- Materialliste (Leitungen mit Ringen, Dosen je Montageart, Geräte, Rahmen, Ports, Verteilerbauteile) als CSV

## Daten
- Jedes Gerät speichert seinen Stand lokal im Browser (eigener Speichername, kommt dem Raumplaner nicht in die Quere).
- Optional: GitHub-Sync über das Wolken-Symbol. Der Stand liegt als `daten.json` im **privaten** Repo `Rilotto/Elektroplaner-daten`. Dafür einen eigenen Token mit Zugriff nur auf dieses Repo anlegen (Contents: Read and write).
- Zusätzliche Sicherung: Menü → „Sicherung speichern“, z. B. nach OneDrive.

Dieses Repo enthält nur den Code, keine Plandaten.

Der Planer ist eine Planungshilfe. Querschnitte, Absicherungen und Regeln prüft eine Elektrofachkraft nach VDE.
