# To-dos

## Einrichtung
- [ ] GitHub Pages einschalten (Settings → Pages → main / root)
- [ ] Privates Repo `Elektroplaner-daten` anlegen, Token nur dafür erstellen und am Tablet verbinden

## Wünsche (Update nach Phase 6)
- [x] Klingeltrafo mit Zuleitung automatisch anlegen, Klingelleitungen im Plan
- [x] Kombination Schalter + Steckdose in einer Achse (z. B. Schalter 105 cm, Steckdose 30 cm)
- [x] Netzwerkkabel im Plan zeichnen
- [x] Leuchten in einer Flucht ausrichten (Hilfslinien beim Verschieben)
- [x] Gesamtanzeige für Probleme und nicht zugewiesene Elemente oben
- [x] „Schaltet“-Liste nach Räumen gegliedert
- [ ] Später: einfache Möbel im Grundriss für bessere Orientierung

## Nächste Version (0.8)
- [ ] Ist und Soll in Elektro getrennt: Ist-Aufnahme und Soll-Plan als eigene Elementbestände je Etage; Soll startet leer, Knopf „Aus Ist übernehmen“ (alle oder ausgewählte Räume); Umbau-Ansicht vergleicht beide; bestehende Daten: Bestand+Entfällt → Ist, Bestand+Neu → Soll
- [ ] Hinweise ignorierbar machen (je Hinweis „Ignorieren“, je Projekt gespeichert, Liste der ignorierten Hinweise wiederherstellbar, Zähler zählt nur offene)
- [ ] Treppenformen: gerade, viertelgewendelt (L), halbgewendelt / zweiläufig mit Podest (U), Wendeltreppe; Lauf links/rechts, Podestgröße; Treppenauge in der Etage darüber in derselben Form
- [ ] Projektstatus: Planung → Umsetzung → Abgeschlossen, jederzeit vor- und zurückschaltbar (Projektmenü und Kopfzeile)
  - Planung: alles bearbeitbar wie bisher
  - Umsetzung: Baufortschritt-Modus steht im Vordergrund; zurück in die Planung jederzeit möglich, der Fortschritt bleibt erhalten
  - Wird nach dem Zurückschalten ein Element mit Fortschritt verschoben, geändert oder gelöscht, markiert die App es (Hinweis „geändert nach Leitung gezogen“ o. Ä.) und setzt betroffene Schritte auf Wunsch zurück
  - Abgeschlossen: Nur-Lesen-Schutz gegen versehentliches Verschieben, abschaltbar
- [ ] Baufortschritt pro Element und Stromkreis: Schritte „Schlitz gestemmt“, „Dose gesetzt“, „Leitung gezogen“, „angeschlossen“, „geprüft“; Fortschrittsanzeige je Raum, Etage und Projekt; Plan färbt Elemente nach Stand; Liste „Was fehlt noch“
- [ ] Wandansicht: Wand antippen → Ansicht von vorne mit allen Dosen in echter Höhe, Türen/Fenster und Installationszonen nach DIN 18015-3; Hinweis bei Dosen außerhalb der Zonen; als Plan druckbar

## Version danach (0.9)
- [ ] Fotos pro Wand (vor dem Verputzen), Ablage in IndexedDB statt localStorage, optional mit GitHub-Sync; in der Wandansicht und im Baufortschritt erreichbar
- [ ] Prüfprotokoll pro Stromkreis: Isolationswiderstand, Schleifenimpedanz / Kurzschlussstrom, FI-Auslösezeit und -strom, Datum, Prüfer; Ausgabe als PDF; Stromkreis gilt im Baufortschritt erst mit Messwerten als „geprüft“
- [ ] Ausstattungs-Check pro Raum nach DIN 18015-2 / RAL-RG 678 (Ausstattungswert 1–3 wählbar): Mindestanzahl Steckdosen, Lichtauslässe, Netzwerk je Raumart und Größe; Fehlendes als (ignorierbarer) Hinweis; Raumart pro Raum einstellbar
- [ ] Bad-Schutzbereiche 0/1/2 um Wanne und Dusche (Wanne/Dusche als Element), Hinweis bei Steckdosen oder Schaltern im Bereich
- [ ] Spannungsfall und Querschnitt pro Stromkreis aus den berechneten Leitungslängen; Warnung, wenn der Querschnitt nicht reicht, mit Vorschlag
- [ ] Große Verbraucher als Vorlagen: Herd (Drehstrom), Wallbox, Wärmepumpe, PV-Einspeisung, Überspannungsschutz, Leerrohre für später; rechnen im Verteiler mit (TE, Schutzorgan, Querschnitt)
- [ ] Kostenschätzung: Preise in der Materialliste hinterlegbar, Summe je Raum, Etage, Projekt; Preise projektübergreifend merken
- [ ] Raumvorlagen: z. B. „Schlafzimmer Standard“, „Küche“, „Bad“ mit typischer Ausstattung, mit einem Tipp in einen Raum setzen, eigene Vorlagen aus einem fertigen Raum speichern

## Version 0.7.0 (erledigt)
- [x] Katalog in Elektro als Klappmenü nach Kategorien
- [x] Mehrere Projekte (Häuser)
- [x] Versionsanzeige mit Änderungsübersicht
- [x] Fehler: Beim Anlegen von Räumen und Zeichnen von Wänden müssen neue Wände zuverlässig an bestehenden Wänden und Ecken einrasten und sich leicht gerade (rechtwinklig, bündig) ausrichten lassen; Fall aus dem Test, wo das kurzzeitig nicht geklappt hat, nachstellen und beheben
- [x] Stromkreis-Art als Symbol: nur Licht, nur Steckdosen, gemischt, Gerät, Außen, Klingeltrafo; in Stromkreisliste, Verteiler-Beschriftung und auf dem LS; Filter in der Verteiler-Ansicht; Prüfung „Licht und Steckdosen eines Raums am selben FI“
- [x] Stromkreis-Übersicht (Verteiler und Elektro) mit Räumen: Elemente je Raum, z. B. „Raum 1: 1 Steckdose · Raum 3: 1 Leuchte“; Räume auch in Stromkreisliste und CSV
- [x] Neues Grundriss-Element „Kabeldurchlass“ (Wand- oder Deckendurchbruch für Leitungen), das die Leitungsführung bevorzugt nutzt
- [x] Unterlage der anderen Etage: Innenwände per Knopf ausblenden (nur Außenwände zeigen)
- [x] Treppen im Grundriss, mit automatischem Treppenauge/Aufgang in der Etage darüber
- [x] Fenster (und Öffnungen) duplizieren
- [x] Leitungsführung verbessern: Wege nie quer durch Räume, sondern entlang der Wände und durch Türen (Wegenetz mit kürzestem Weg zum Verteiler); Zuleitungen bündeln, gemeinsame Strecken nur einmal zeichnen mit Anzahl; Einspeisepunkt einer Schaltung automatisch an der Schaltstelle mit dem kürzesten Weg zum Verteiler; gilt auch für Verbindungen zwischen Schaltern, Klingel- und Netzwerkleitungen

## Phasen
- [x] 1. Grundriss und Etagen
- [x] 2. Elemente und Ist-Aufnahme (Schaltzeichen, Höhen, Montageart, Legende, Ebene Elektro, Varianten), erste Fassung
- [x] 3. Verteiler und Stromkreise, erste Fassung
- [x] 4. Leitungen und Mengen, erste Fassung
- [x] 5. Netzwerk, Klingel, Außen, Eltako, erste Fassung
- [x] 6. Pläne und Ausgaben, erste Fassung
- [ ] 7. Automatische Verdrahtung (vorerst nicht geplant)
