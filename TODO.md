# To-dos

## Arbeitsregeln für jedes Update
1. **Baut auf der Vorversion auf:** Jedes Update startet vom aktuellen Stand von `main` (der zuletzt veröffentlichten Version) und ändert nur, was das Update betrifft. Keine Neuschreibung von Teilen, die nicht dazugehören.
2. **Folgt dem Designkonzept** (Projektdoku „Elektroplaner-Designkonzept“): Plan als Arbeitsfläche; Arbeitsschritte ① Grundriss ② Elektro ③ Verteiler ④ Ausgabe; Plan-Werkzeuge schweben am Plan (Stand/Varianten/Ebenen oben links, Etagen rechts oben, Werkzeuge unten links); Element-Daten im Seitenfeld; Akzentblau nur für Bedienbares und Ausgewähltes; Statusfarben nur mit Bedeutung; Ziele ≥ 44 px; kurze Texte in Du-Form. Neue Funktionen bekommen ihren Platz in dieser Struktur (z. B. neue Ebenen ins Menü „Ebenen“, neue Ausgaben in ④ Ausgabe), keine neuen Knöpfe in der Kopfzeile.
3. **Weicht ein Wunsch vom Konzept ab**, wird das vorher kurz angesprochen und bei Zustimmung im Designkonzept nachgetragen.
4. **Zu jedem Update:** Versionsnummer + Änderungsliste (CHANGELOG in der App), Service-Worker-Cache hochzählen, bestehende Daten weiter lesbar (Migration in `upgrade`), Test mit der Testwohnung im Quer- und Hochformat, danach Projektdoku „Stand“ und diese Liste aktualisieren.

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

## Eigene Linie: Teilen mit Freunden
- [ ] Tutorial / Einführung für neue Nutzer: geführte Tour beim ersten Start (überspringbar, jederzeit im Menü „Einführung“ wieder startbar), kurze Schritte mit Hervorhebung: Projekt anlegen → Raum zeichnen/andocken → Tür/Fenster → Elektro: Element setzen → Schalter mit Leuchte verbinden → Stromkreis anlegen → Verteiler → Material/Pläne ausgeben
- [ ] Beispielprojekt direkt in der App ladbar (Projekte → „Beispiel öffnen“), damit Freunde ohne Datei loslegen können; Grundlage: die Mini-Testwohnungen aus `beispiele/` bzw. die Testwohnung 4 Zimmer (Idee vom Nutzer bestätigt)
- [ ] Kurze Hilfe-Seite (Was ist was, Gesten, Symbole) und Hinweis, dass die App keine Elektrofachkraft ersetzt
- [ ] Teilen: Link auf GitHub Pages, Daten bleiben lokal auf dem Gerät des Freundes; Sicherung als Datei zum Weitergeben

## Bedienung und Design
- [x] Bedienkonzept überarbeiten: Designkonzept in der Projektdoku „Elektroplaner-Designkonzept“, Testversion im Branch `design` (Artifact „Elektroplaner Design-Test“)
- [x] `design` in `main` übernommen (0.7.1)
- [ ] Offene Punkte aus dem Designkonzept (Auswahlfeld mit „Mehr“, feste Aktionsleiste unten im Seitenfeld, Meldungen unten); Raumränder nur bei gewähltem Stromkreis kommt mit 0.7.4

## Fahrplan (mehrere kleine Zwischenschritte)

## 0.7.1 – Neues Bedienkonzept (erledigt)
- [x] Arbeitsschritte ① Grundriss ② Elektro ③ Verteiler ④ Ausgabe, Ausgabe mit Druckvorschau
- [x] Werkzeuge, Stand, Ebenen und Etagen am Plan; Kopfzeile aufgeräumt
- [x] Elementsuche im Katalog (vorgezogen aus der alten Liste)
- [x] ~~Ansicht je Arbeitsschritt gemerkt~~ – in 0.7.2.1 auf Wunsch wieder entfernt: die Ansicht bleibt beim Schrittwechsel, wie gewählt

## 0.7.2 – Maße, Hinweise, Wippen (erledigt)
- [x] Maße beim gewählten Wandelement: Maßlinien im Plan bis Raumecke bzw. Tür-/Fenster-/Durchgangskante; im Seitenfeld „Abstand links“ / „Abstand rechts“ (mit Blick auf die Wand, bis Dosenmitte) statt „Abstand Wandanfang“, beide editierbar
- [x] Deckenelemente: Maßlinien zur nächsten Wand in x und y, im Seitenfeld alle vier Abstände
- [x] Hinweise ignorierbar (je Hinweis „Ignorieren“, gespeichert im Projekt als `S.ignored` über den Hinweistext; ändert sich der Hinweis, erscheint er wieder; Bereich „Ignorierte Hinweise“ mit „Wieder zeigen“; Zähler zählt nur offene)
- [x] Serienschalter: Zuordnung je Leuchte gab es schon (als „Kreis 1/2“, im Schaltbild berücksichtigt), jetzt als „Wippe 1/2“ benannt

## 0.7.3 – Schalter verknüpfen und Grundausstattung (erledigt)
- [x] Schalter auf Schalter/Dose an derselben Wand ziehen → Auswahl „Mehrfachkombination“ (gemeinsamer Rahmen, bis 5-fach, `it.frame`), „Serienschalter“ (zwei Ausschalter → ein Serienschalter, Leuchten des gezogenen Schalters auf Wippe 2) oder „Übereinander“ (Schalter + Steckdose, bestehende Kombination); Lösen bzw. „In zwei Ausschalter teilen“ im Seitenfeld; Material zählt Rahmen der Kombination als einen n-fach-Rahmen
- [x] ⊕-Punkt am gewählten Schalter auf eine Leuchte ziehen verbindet bzw. trennt sie (auch Rollladentaster → Motor)
- [x] Grundausstattung: TV/SAT-Antennendose, Leerdose mit Leerrohr, Rollladentaster + Rollladenmotor (Leitung NYM-J 4×1,5, Hinweise bei fehlender Zuordnung), Video-Innenstation (an der Klingelleitung)
- [x] Einstellung „Schalterdosen als tiefe Elektronikdosen“ (Menü → Rechenvorgaben), Material passt sich an; N und PE in jeder Schalterdose stehen schon im Schaltbild („N, PE geklemmt“) und jetzt auch im Hinweis der Materialliste

## 0.7.4 – Leitungen, Hervorheben, Setzen, Ausgabe (im Branch `vorschau`, wartet auf Okay)
- [x] Bündel antippen → Leitungen einzeln aufgefächert mit Stromkreis und Leitungstyp; Seitenfeld mit Liste, Schlitzbreite/-tiefe und Leerrohrgröße; Hinweis ab 80 mm Breite
- [x] Alle Starkstromleitungen zählen im Bündel (Zuleitung, zur Leuchte, Korrespondierende, Rollladen); Daten- und Klingelleitungen als eigenes Bündel, im Plan mit Abstand (Standard 10 cm) parallel gezeichnet; Einstellungen in Menü → Rechenvorgaben
- [x] Schlitzliste in ④ Ausgabe (je Raum zusammengefasst) und als CSV
- [x] Leitungsverlauf selbst festlegen für Schaltungslinien (Schalter ↔ Leuchte, Korrespondierende): Linie antippen, ⊕ ziehen setzt Knick, Punkte verschieben, doppelt antippen löscht, „Automatisch“ setzt zurück; Längen rechnen mit (`S.routes`)
- [x] Verlegung je Schaltung „an der Wand entlang“ oder „über die Decke direkt“ (`sw.ceil`), Reihenfolge der Leuchten mit ↑↓ (`lseq`)
- [x] Stromkreis hervorheben (Ring, kräftige Leitungen, Rest blass, Raumtönung, Farbpunkt an der Etage, Infozeile); im Reiter Stromkreise wählt ein Tipp aufs Element dessen Stromkreis, Tipp ins Leere hebt auf; im Verteiler „Im Plan zeigen“
- [x] Mehrfachkombination hintereinander gezeichnet
- [x] Setzen endet nach einem Element, neues Element ist gewählt; „📌 Mehrere setzen“; Tipp auf vorhandenes Element beendet das Setzen; Anzeige unten „Setzen: … ✕“ (auch für Zuordnen), Esc beendet
- [x] Ausgabe: Räume weiß, Wände kräftiger, Schrift im Bild nicht mehr mit Serifen
- [x] Materialliste als Reiter in ④ Ausgabe, Eintrag „Materialliste“ im ☰-Menü
- [ ] Offen (siehe Fragenliste): Hinweis „Datenleitung zu nah an Strom“ erst mit selbst verlegten Datenleitungen; eigener Verlauf vorerst nur für Schaltungslinien

## 0.7.5 – Dosenbelegung und Abzweigdosen (im Branch `vorschau`, wartet auf Okay)
- [x] Einstellung Verdrahtung (Menü → Rechenvorgaben): „Mit Abzweigdosen“ (Standard für neue Projekte), „Abzweigdosen vorschlagen“, „Ohne Abzweigdosen“; bestehende Projekte mit Elementen starten mit „Ohne“ (`S.settings.wiring`)
- [x] Mit Abzweigdosen: je Schaltung automatisch eine Abzweigdose in der Deckenzone neben dem ersten Schalter (Zuleitung → Abzweigdose → Schalter und Leuchten); antippen → „Festlegen (zum Verschieben)“ macht daraus ein echtes Element, „Hier keine Abzweigdose“ (`noAbz`)
- [x] Vorschlagen: gestrichelte Punkte mit ? an Schalterdosen mit zu vielen Leitungen, „Übernehmen“ setzt die Abzweigdose
- [x] Abzweigdose als Element im Katalog (Suchwörter Verteilerdose, Klemmdose), Feld „Schaltung über diese Dose“ (`serves`), Hinweis zur Zugänglichkeit
- [x] Dosenbelegung im Seitenfeld jeder Wanddose: ankommende Leitungen mit Stromkreis, Klemmen je Leiter (L, N, PE, S, K1/K2)
- [x] Hinweis bei vollen Dosen (mehr als 4 Leitungen, tiefe Dose 5, Abzweigdose 8); Material zählt Abzweigdosen und Klemmen-Sätze

## 0.8 – Ist und Soll getrennt, Treppen, Wandansicht (im Branch `vorschau`, wartet auf Okay)
- [x] Ist-Aufnahme und Soll-Plan als getrennte Elementlisten je Etage (`f.istLayout`, Soll = Varianten), eigene Stromkreise (`S.istCircuits` / `S.circuits`), Verteiler, Hinweise, Material, Schlitze und Ausgaben je Plan; Plan-Umschalter auch in ③ Verteiler und bei Material/Schlitzen
- [x] Bestehende Daten: Bestand + Entfällt → Ist (mit eigenen Stromkreis-Kopien), Bestand + Neu → Soll, Bestand im Soll mit dem Ist verknüpft (`src`); einmalig beim Laden (`split08`)
- [x] „Aus Ist übernehmen …“ im Soll (Räume wählbar, Stromkreise mit übernehmen), übernommene Elemente bleiben verknüpft
- [x] Umbau-Ansicht vergleicht: bleibt · entfällt · neu · versetzt (orange, gestrichelte Linie von der alten Lage); dort nur ansehen, bearbeiten in Ist oder Soll
- [x] Treppenformen: gerade, viertelgewendelt (L mit Podest), halbgewendelt (U mit Podest, Treppenauge-Breite), Wendeltreppe; Richtung links/rechts; Treppenauge oben in derselben Form
- [x] Wandansicht: aus einer gewählten Wanddose („Wandansicht“) oder einer Wand im Grundriss (Seite A/B); Raumbreite × Raumhöhe, Türen/Fenster, Installationszonen nach DIN 18015-3, Dosen außerhalb der Zonen orange mit Hinweis; Dosen waagrecht und senkrecht ziehen; als Bild speichern; andere Wandseite

## 0.8.1 – Antworten aus dem Nachtlauf (im Branch `vorschau`)
- [x] Browser darf die App nicht selbst abdunkeln (`color-scheme`), Ausgabe-Vorschau bleibt hell (graue Ausgabe vermutlich durch das automatische Dunkel-Design des Tablet-Browsers)
- [x] Leitungswege bleiben immer sichtbar (Entscheidung), Hervorhebung blendet nur ab
- [x] Abzweigdose direkt über dem ersten Schalter (Deckenzone), im Plan hinter dem Schalter gezeichnet; Abzweigdose voll ab 6 Leitungen; K1/K2 in der Dosenbelegung bei Wechsel/Kreuz über Abzweigdose
- [x] Umstellung bestehender Daten: Bestand kommt nur in die Ist-Aufnahme, der Soll-Plan enthält nur Neues
- [x] Umbau-Ansicht markiert geänderte Elemente (Art, Anzahl, Höhe, schaltbar, Montage) in Violett
- [x] Treppen viertel- und halbgewendelt ohne Podest (gewendelte Stufen)
- [ ] Offen: Frage 3 (eigener Verlauf auch für Zuleitungen/LAN) – neu erklärt, Antwort steht aus

## 0.8.2 – Bugfix Wände verknüpfen (erledigt)
- [x] Beim Zeichnen schließt sich der Zug zuverlässig: Fangradius für vorhandene Ecken beim Zeichnen größer (bildschirmbezogen, mind. ca. 15 cm), besonders für den Startpunkt des Zugs
- [x] Fluchten beim Zeichnen bevorzugen Startpunkt und vorherigen Punkt (gerade Wände), auch wenn das Raster auf einen anderen Wert runden würde
- [x] Ecke auf Ecke ziehen (Verknüpfen im Nachhinein): Wände, die dadurch nur leicht schief werden (unter ca. 3°), werden automatisch begradigt – die angrenzenden Ecken rücken mit, statt eine schiefe Wand zu lassen (Bild des Nutzers: 5 cm Versatz → schiefe Außenwand)
- [x] Zusätzlich Knopf „Raum begradigen“ im Raum-Seitenfeld

## 0.8.8 – Wünsche vom Aufmaß
- [ ] Mehrfachkombination: alle Teile bekommen eine gemeinsame Montagehöhe, gemessen vom obersten Punkt der Kombination; oben sitzt immer der Schalter (Nutzerwunsch 25.10.2026)

## 0.8.7 – Fenster und Türen innen bemessen (erledigt)
- [x] Abstände von der inneren Raumecke (ganze Raumseite) statt von der Wandachse, beschriftet links/rechts bzw. oben/unten; bei Innenwänden wählbar, in welchem Raum gemessen
- [x] Schloss je Wert: Breite, Höhe, Abstände, Brüstung; feste Abstände bleiben bei Wandänderungen, sind beide Abstände fest, passt sich die Breite an (außer sie ist auch fest)
- [ ] Später: Schlösser auch für Abstände der Elektro-Elemente

## 0.8.6 – Raumseiten mit eigenem Maß (erledigt)
- [x] Innenmaße im Plan je ganzer gerader Raumseite (Abschnitte an T-Stößen werden zusammengefasst)
- [x] Seitenfeld der Wand: „Seite Raum“ = ganze Raumseite, jede Seite und die Achse mit eigenem Schloss
- [x] Eingabe einer Raumseite verschiebt das Ende der ganzen Seite; die andere Seite derselben Trennwand bleibt unabhängig

## 0.8.5 – Feste Maße (erledigt)
- [x] Eingegebene Wandlängen werden automatisch mit Schloss festgehalten (Schloss an der Maßzahl im Plan), Knopf „Maß festhalten / lösen“ im Seitenfeld der Wand
- [x] Länge eingeben: verschiebt das gewählte Ende; würde das ein festes Maß ändern, automatisch das andere Ende; geht beides nicht, Hinweis
- [x] Ziehen von Ecken und Wänden stoppt, bevor ein festes Maß sich ändert; „Raum begradigen“ ebenso

## 0.8.4 – Notfall: Wandlänge eingeben (erledigt)
- [x] Länge eingeben verschiebt nicht mehr alles rechts/unterhalb im ganzen Plan (verzog andere Räume), sondern nur die Querwand am gewählten Ende, wie beim Ziehen
- [x] Wählbar im Seitenfeld der Wand: welches Ende sich bewegt (links/rechts bzw. oben/unten)

## 0.8.3 – Notizen (erledigt)
- [x] Notizen als Stecknadel im Plan oder allgemein zum Projekt; Knopf „Notizen“ unten am Plan mit Übersicht, Bearbeiten im Seitenfeld, Erledigt, Verschieben, Löschen
- [x] Ein-/Ausblenden unter „Ebenen“, Eintrag im ☰-Menü für ③/④
- [ ] Später: Notizen in ④ Ausgabe (Liste, optional Nadeln im Plan)
- [ ] Später: Foto an Notiz (mit den Fotos aus 0.9), Notiz an ein Element hängen

## 0.9 – Umsetzung auf der Baustelle
- [ ] Projektstatus: Planung → Umsetzung → Abgeschlossen, jederzeit vor- und zurückschaltbar (Projektmenü und Kopfzeile)
  - Planung: alles bearbeitbar wie bisher
  - Umsetzung: Baufortschritt steht im Vordergrund; zurück in die Planung jederzeit möglich, Fortschritt bleibt erhalten
  - Wird danach ein Element mit Fortschritt geändert, verschoben oder gelöscht, markiert die App es („geändert nach Leitung gezogen“) und setzt betroffene Schritte auf Wunsch zurück
  - Abgeschlossen: Nur-Lesen-Schutz, abschaltbar
- [ ] Baufortschritt pro Element und Stromkreis: „Schlitz gestemmt“, „Dose gesetzt“, „Leitung gezogen“, „angeschlossen“, „geprüft“; Fortschritt je Raum, Etage, Projekt; Plan färbt nach Stand; Liste „Was fehlt noch“
- [ ] Fotos pro Wand (vor dem Verputzen), Ablage in IndexedDB statt localStorage, optional mit GitHub-Sync; in Wandansicht und Baufortschritt erreichbar
- [ ] Prüfprotokoll pro Stromkreis: Isolationswiderstand, Schleifenimpedanz / Kurzschlussstrom, FI-Auslösezeit und -strom, Datum, Prüfer; PDF; Stromkreis gilt erst mit Messwerten als „geprüft“
- [ ] Eigenen Leitungsverlauf auch für Zuleitungen (Verteiler → erstes Element, Element → Element) und LAN-Kabel (Datenverteiler → Netzwerkdose): Linie antippen, Knickpunkte ziehen wie bei Schaltungslinien; Längen, Bündel und Schlitzliste rechnen mit; dann auch Hinweis „Datenleitung zu nah an Starkstrom“ (Antwort des Nutzers auf Frage 3)
- [ ] Grundriss importieren (Wunsch: Grundriss vom Architekten/Vermieter nachträglich übernehmen), in Stufen:
  - Stufe 1 – Unterlage: Bild (JPG/PNG, Foto vom Plan) oder PDF als Unterlage je Etage laden (Grundriss → Etage → „Grundriss-Unterlage“); Maßstab über zwei angetippte Punkte und ein bekanntes Maß setzen (z. B. Außenwand 10,24 m); drehen, verschieben, Deckkraft; danach Wände mit der vorhandenen Zeichenhilfe nachzeichnen (Einrasten an Linien der Unterlage später); Ablage in IndexedDB wie die Fotos, Sync optional
  - Stufe 2 – CAD-Import: DXF-Datei (vom Architekten) einlesen, Linien/Polylinien eines gewählten Layers als Wände übernehmen (Wanddicke aus parallelen Linien erkennen), Türen/Fenster aus Blöcken soweit möglich
  - Stufe 3 – Assistent: aus der Bild-Unterlage Wände vorschlagen (Linien erkennen), Vorschläge antippen zum Übernehmen
  - Formate (Wunsch: alle möglichen berücksichtigen):
    - Bilder: JPG, PNG, WebP, HEIC (Handyfoto), GIF/BMP → Unterlage (Stufe 1, Assistent Stufe 3)
    - PDF: Raster-PDF → Unterlage; Vektor-PDF (vom Architekten) → Linien direkt auslesen und als Wände vorschlagen (pdf.js)
    - SVG → Linien/Pfade als Wände vorschlagen
    - DXF → Wände aus Layern (Stufe 2)
    - DWG → nicht offen lesbar; Weg über Umwandlung in DXF (Hinweis mit kostenlosem Konverter) oder später eine DWG-Bibliothek
    - IFC (BIM-Modell) → Wände mit Dicke, Türen, Fenster und Räume direkt übernehmen
    - Raumplaner (eigene App, JSON) → Wände, Türen, Fenster und Räume 1:1 übernehmen
    - Exporte anderer Apps (z. B. magicplan, Floorplanner, RoomScan) → meist DXF, PDF oder Bild, damit abgedeckt
  - Bestehende Etage: Unterlage über den gezeichneten Grundriss legen, um Abweichungen zu sehen; Import ersetzt nie ungefragt vorhandene Wände


## 0.10 – Planung prüfen und beschleunigen
- [ ] Ausstattungs-Check pro Raum nach DIN 18015-2 / RAL-RG 678 (Ausstattungswert 1–3): Mindestanzahl Steckdosen, Lichtauslässe, Netzwerk je Raumart und Größe; Raumart pro Raum; Fehlendes als ignorierbarer Hinweis
- [ ] Bad-Schutzbereiche 0/1/2 um Wanne und Dusche (Wanne/Dusche als Element), Hinweis bei Dosen oder Schaltern im Bereich
- [ ] Spannungsfall und Querschnitt pro Stromkreis aus den Leitungslängen; Warnung mit Vorschlag
- [ ] Große Verbraucher als Vorlagen: Herd (Drehstrom), Wallbox, Wärmepumpe, PV-Einspeisung, Überspannungsschutz; rechnen im Verteiler mit
- [ ] Kostenschätzung: Preise in der Materialliste, Summe je Raum, Etage, Projekt; Preise projektübergreifend merken
- [ ] Raumvorlagen: „Schlafzimmer Standard“, „Küche“, „Bad“ …, eigene Vorlagen aus einem fertigen Raum speichern

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

## 1.x – Module (Idee, weit fortgeschritten)

### Aufbau: zwei Arten von Modulen
Damit sich nichts vermischt, wenn z. B. ein Rollladenmotor über einen Zigbee-Aktor und einen normalen Taster gesteuert wird:
- **Was wird gesteuert (Funktionsmodule):** Beschattung/Rollladen, Heizung, Sicherheit, Energie, Medien, Außenbereich. Sie bringen die Geräte und Verbraucher mit (Motor, Stellantrieb, Kamera …) und die Gruppen, in denen sie zusammengefasst werden.
- **Womit wird gesteuert (Technikmodule):** konventionell (immer da), Eltako (schon da), Zigbee/Home Assistant, KNX, später ggf. Matter/Thread oder WLAN (Shelly). Sie bringen keine Verbraucher mit, sondern Aktoren, Bedienstellen, Leitungen und Prüfungen.
- Jede Gruppe (Lichtschaltung, Rollladengruppe, Heizkreis) bekommt ein Feld **„Steuerung“** mit den eingeschalteten Techniken. Die Wahl entscheidet, welche Aktoren gebraucht werden (Unterputz in der Dose oder Reiheneinbau im Verteiler), welche Leitungen und welches Material anfallen.
- Bedienstellen bleiben gemischt erlaubt: normaler Taster am Aktor-Eingang, Funktaster, Wandschalter mit Zigbee-Einsatz.
- Module pro Projekt in den Projekteinstellungen ein-/ausschaltbar; Code bleibt in einer Datei mit interner Modul-Registry, erst bei Bedarf als eigene .js nachladen.

### Technikmodule
- [ ] Zigbee / Home Assistant (Wunsch des Nutzers): Koordinator (USB-Stick am HA-Server, Standort im Plan), Unterputz-Aktoren in Schalter-/Geräteposition (Licht, Dimmer, Rollladen), Funktaster, Sensoren (Tür/Fenster, Bewegung, Temperatur); Prüfung: Neutralleiter und tiefe Dose am Aktor-Ort; Mesh-Hinweis (netzbetriebene Geräte sind Router, Abstand zum Koordinator/nächsten Router); HA-Server im Datenverteiler (Netzwerk, Steckdose); Geräteliste als CSV
- [ ] KNX: Busleitung (grün, eigene Linienführung), Aktoren und Netzteil im Verteiler mit TE, Taster mit Tastenbelegung, Präsenzmelder, Gruppenadressen-Liste als CSV für die ETS

### Funktionsmodule
- [ ] Beschattung / Rollladen (zuerst): Motor am Fenster andockend, Einzel-/Gruppen-/Zentralsteuerung, Wind-/Sonnen-/Zeitautomatik, Motorleitung (z. B. 4×1,5), Steuerung über Technikmodul, Steuerungsschema je Gruppe
- [ ] Heizung: Raumthermostate, Stellantriebe Fußbodenheizung, Heizkreisverteiler mit Klemmleiste
- [ ] Sicherheit: Rauchmelder-Pflichtprüfung (Schlafräume, Kinderzimmer, Flure), Alarmanlage, Kameras (PoE → Netzwerk)
- [ ] Energie: PV, Speicher, Wallbox, Wärmepumpe, Zählerplatz nach TAB
- [ ] Medien: SAT/Antenne (Koax-Stern, Multischalter), Lautsprecher / Multiroom
- [ ] Außenbereich: Garten- und Wegebeleuchtung, Erdkabel NYY mit Längen

## Später
- [ ] Einfache Möbel im Grundriss für bessere Orientierung (aus dem Raumplaner)
