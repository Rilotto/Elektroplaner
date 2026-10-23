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

## Daten
- Jedes Gerät speichert seinen Stand lokal im Browser (eigener Speichername, kommt dem Raumplaner nicht in die Quere).
- Optional: GitHub-Sync über das Wolken-Symbol. Der Stand liegt als `daten.json` im **privaten** Repo `Rilotto/Elektroplaner-daten`. Dafür einen eigenen Token mit Zugriff nur auf dieses Repo anlegen (Contents: Read and write).
- Zusätzliche Sicherung: Menü → „Sicherung speichern“, z. B. nach OneDrive.

Dieses Repo enthält nur den Code, keine Plandaten.

Der Planer ist eine Planungshilfe. Querschnitte, Absicherungen und Regeln prüft eine Elektrofachkraft nach VDE.
