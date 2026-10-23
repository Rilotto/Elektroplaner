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

## Fahrplan (mehrere kleine Zwischenschritte)

## 0.7.1 – Kleinigkeiten, die beim Testen sofort helfen
- [ ] Suchleiste im Elemente-Katalog: Suche über Namen, Gruppen und Stichwörter (z. B. „Klingel“, „Herd“, „PoE“, „Zigbee“), Treffer aus allen Gruppen, aufgeklappt; Tippen setzt das Element wie bisher; letzte/zuletzt genutzte Elemente oben
- [ ] Maße beim ausgewählten Wandelement: Maßketten im Plan von der Dose bis zur nächsten Raumecke bzw. Tür-/Fensterkante links und rechts (im Raum gemessen, nicht ab Wandanfang); im Panel „Abstand links“ / „Abstand rechts“ (Raumseite) statt „Abstand Wandanfang“, beide editierbar
- [ ] Gleiches für Deckenelemente: Abstand zu den nächsten Wänden in x und y beim Auswählen
- [ ] Hinweise ignorierbar machen (je Hinweis „Ignorieren“, je Projekt gespeichert, Liste der ignorierten wiederherstellbar, Zähler zählt nur offene)
- [ ] Serienschalter: je Leuchte festlegen, an welcher Wippe sie hängt (Wippe 1 / 2), im Schaltbild und in der Leitungsliste

## 0.7.2 – Schalter verknüpfen und Grundausstattung ergänzen
- [ ] Schalter verknüpfen per Drag and Drop: Schalter auf Schalter ziehen → „Mehrfachkombination“ (gemeinsamer 2-/3-fach-Rahmen, z. B. Licht innen + Licht außen) oder „Serienschalter“ (ein Einsatz, zwei Wippen); auch Schalter + Steckdose als Kombination; Lösen per Knopf; Material zählt Rahmen, Einsätze und Dosen richtig
- [ ] Schalter → Leuchte per Ziehen zuordnen
- [ ] Grundausstattung (immer da, kein Modul) ergänzen: TV/SAT-Antennendose, Leerdose mit Leerrohr (für später), Rollladenschalter/-taster und Motoranschluss (einfache Ausführung), Video-Türsprechanlage / Innenstation; Türsprechanlage und Rauchwarnmelder sind schon drin
- [ ] Neutralleiter in jeder Schalterdose als Projekteinstellung (Standard an, wichtig für spätere Smart-Home-Aktoren); Schalterdosen wahlweise als tiefe Elektronikdosen im Material

## 0.7.3 – Leitungen: Bündel aufklappen und Verlauf selbst anpassen
- [ ] Bündel antippen → fächert sich auf: alle Leitungen dieser Strecke einzeln nebeneinander gezeichnet, jede mit Farbe und Beschriftung (Leitungstyp, Stromkreis-Nr., Ziel/Raum); klappt wieder zu, sobald woanders getippt wird
- [ ] Alle Leitungsarten bündeln, nicht nur Stromkreis-Zuleitungen: auch Schalter→Leuchte, Klingel, Netzwerk, Bus, damit die Zahl im Bündel stimmt
- [ ] Datenleitungen (CAT, Telefon, Koax) getrennt von Starkstrom führen: eigenes Wegenetz-Bündel, eigener Schlitz; beim automatischen Verlauf parallel mit einstellbarem Mindestabstand (Standard z. B. 10 cm, vgl. DIN EN 50174-2) statt in derselben Strecke; Kreuzungen möglichst rechtwinklig; Hinweis, wenn eine Datenleitung (auch selbst verschoben) zu nah an einer Stromleitung liegt. Klingel und Bus (Kleinspannung) ebenfalls getrennt, als Einstellung
- [ ] Infokasten zum Bündel: Anzahl je Leitungstyp (z. B. 3× NYM-J 3×1,5, 2× NYM-J 5×1,5; Datenleitungen haben eigene Bündel), Summe der Außendurchmesser (Tabelle mit ca.-Werten je Typ, in den Einstellungen anpassbar), daraus empfohlene Schlitzbreite/-tiefe bei Verlegung nebeneinander bzw. Leerrohrgröße; Hinweis bei zu breitem Schlitz (Statik, ggf. zwei Schlitze oder Leerrohr)
- [ ] Schlitzliste je Raum/Wand als Tabelle und CSV (für die Baustelle), später auch in der Wandansicht
- [ ] Verlauf selbst anpassen: Leitung antippen → Ziehpunkte erscheinen; Strecke ziehen erzeugt einen Knick (rastet auf 90° und an Wänden/anderen Leitungen ein, damit Bündel entstehen); Knickpunkt doppelt antippen löscht ihn; „Automatisch“ setzt die Strecke zurück
- [ ] Gespeichert je Teilstück (von Element zu Element), Längen und Material rechnen mit dem eigenen Verlauf; eigene Strecken werden leicht anders markiert
- [ ] Verlegeart je Strecke: „an der Wand“ (heute) oder „über die Decke direkt“ (z. B. Leuchte zu Leuchte in einer Reihe, ohne Abstecher zur Wand); auch als Voreinstellung je Stromkreis/Schaltung
- [ ] Reihenfolge der Leuchten in einer Schaltung festlegen (wer an wem hängt), damit Ketten Leuchte→Leuchte sinnvoll laufen

## 0.8 – Ist und Soll getrennt, Treppen, Wandansicht
- [ ] Ist und Soll in Elektro getrennt: Ist-Aufnahme und Soll-Plan als eigene Elementbestände je Etage; Soll startet leer, Knopf „Aus Ist übernehmen“ (alle oder ausgewählte Räume); Umbau-Ansicht vergleicht beide; bestehende Daten: Bestand+Entfällt → Ist, Bestand+Neu → Soll
- [ ] Treppenformen: gerade, viertelgewendelt (L), halbgewendelt / zweiläufig mit Podest (U), Wendeltreppe; Lauf links/rechts, Podestgröße; Treppenauge in der Etage darüber in derselben Form
- [ ] Wandansicht: Wand antippen → Ansicht von vorne mit allen Dosen in echter Höhe, Türen/Fenster und Installationszonen nach DIN 18015-3; Hinweis bei Dosen außerhalb der Zonen; als Plan druckbar

## 0.9 – Umsetzung auf der Baustelle
- [ ] Projektstatus: Planung → Umsetzung → Abgeschlossen, jederzeit vor- und zurückschaltbar (Projektmenü und Kopfzeile)
  - Planung: alles bearbeitbar wie bisher
  - Umsetzung: Baufortschritt steht im Vordergrund; zurück in die Planung jederzeit möglich, Fortschritt bleibt erhalten
  - Wird danach ein Element mit Fortschritt geändert, verschoben oder gelöscht, markiert die App es („geändert nach Leitung gezogen“) und setzt betroffene Schritte auf Wunsch zurück
  - Abgeschlossen: Nur-Lesen-Schutz, abschaltbar
- [ ] Baufortschritt pro Element und Stromkreis: „Schlitz gestemmt“, „Dose gesetzt“, „Leitung gezogen“, „angeschlossen“, „geprüft“; Fortschritt je Raum, Etage, Projekt; Plan färbt nach Stand; Liste „Was fehlt noch“
- [ ] Fotos pro Wand (vor dem Verputzen), Ablage in IndexedDB statt localStorage, optional mit GitHub-Sync; in Wandansicht und Baufortschritt erreichbar
- [ ] Prüfprotokoll pro Stromkreis: Isolationswiderstand, Schleifenimpedanz / Kurzschlussstrom, FI-Auslösezeit und -strom, Datum, Prüfer; PDF; Stromkreis gilt erst mit Messwerten als „geprüft“

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
