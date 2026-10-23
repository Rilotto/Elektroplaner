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
- [ ] Beispielprojekt „Testwohnung 4 Zimmer“ direkt in der App ladbar (Projekte → „Beispiel öffnen“), damit Freunde ohne Datei loslegen können
- [ ] Kurze Hilfe-Seite (Was ist was, Gesten, Symbole) und Hinweis, dass die App keine Elektrofachkraft ersetzt
- [ ] Teilen: Link auf GitHub Pages, Daten bleiben lokal auf dem Gerät des Freundes; Sicherung als Datei zum Weitergeben

## Bedienung und Design
- [x] Bedienkonzept überarbeiten: Designkonzept in der Projektdoku „Elektroplaner-Designkonzept“, Testversion im Branch `design` (Artifact „Elektroplaner Design-Test“)
- [x] `design` in `main` übernommen (0.7.1)
- [ ] Offene Punkte aus dem Designkonzept (Auswahlfeld mit „Mehr“, feste Aktionsleiste unten im Seitenfeld, Meldungen unten, Raumränder nur bei gewähltem Stromkreis)

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

## 0.7.4 – Leitungen: Bündel aufklappen und Verlauf selbst anpassen
- [ ] Bündel antippen → fächert sich auf: alle Leitungen dieser Strecke einzeln nebeneinander gezeichnet, jede mit Farbe und Beschriftung (Leitungstyp, Stromkreis-Nr., Ziel/Raum); klappt wieder zu, sobald woanders getippt wird
- [ ] Alle Leitungsarten bündeln, nicht nur Stromkreis-Zuleitungen: auch Schalter→Leuchte, Klingel, Netzwerk, Bus, damit die Zahl im Bündel stimmt
- [ ] Datenleitungen (CAT, Telefon, Koax) getrennt von Starkstrom führen: eigenes Wegenetz-Bündel, eigener Schlitz; beim automatischen Verlauf parallel mit einstellbarem Mindestabstand (Standard z. B. 10 cm, vgl. DIN EN 50174-2) statt in derselben Strecke; Kreuzungen möglichst rechtwinklig; Hinweis, wenn eine Datenleitung (auch selbst verschoben) zu nah an einer Stromleitung liegt. Klingel und Bus (Kleinspannung) ebenfalls getrennt, als Einstellung
- [ ] Infokasten zum Bündel: Anzahl je Leitungstyp (z. B. 3× NYM-J 3×1,5, 2× NYM-J 5×1,5; Datenleitungen haben eigene Bündel), Summe der Außendurchmesser (Tabelle mit ca.-Werten je Typ, in den Einstellungen anpassbar), daraus empfohlene Schlitzbreite/-tiefe bei Verlegung nebeneinander bzw. Leerrohrgröße; Hinweis bei zu breitem Schlitz (Statik, ggf. zwei Schlitze oder Leerrohr)
- [ ] Schlitzliste je Raum/Wand als Tabelle und CSV (für die Baustelle), später auch in der Wandansicht
- [ ] Verlauf selbst anpassen: Leitung antippen → Ziehpunkte erscheinen; Strecke ziehen erzeugt einen Knick (rastet auf 90° und an Wänden/anderen Leitungen ein, damit Bündel entstehen); Knickpunkt doppelt antippen löscht ihn; „Automatisch“ setzt die Strecke zurück
- [ ] Gespeichert je Teilstück (von Element zu Element), Längen und Material rechnen mit dem eigenen Verlauf; eigene Strecken werden leicht anders markiert
- [ ] Verlegeart je Strecke: „an der Wand“ (heute) oder „über die Decke direkt“ (z. B. Leuchte zu Leuchte in einer Reihe, ohne Abstecher zur Wand); auch als Voreinstellung je Stromkreis/Schaltung
- [ ] Reihenfolge der Leuchten in einer Schaltung festlegen (wer an wem hängt), damit Ketten Leuchte→Leuchte sinnvoll laufen

## 0.7.5 – Dosenbelegung und Abzweigdosen
- [ ] Dosenbelegung: jede Schalter-/Geräte-/Abzweigdose antippen → Seitenfeld zeigt, welche Leitungen ankommen (von wo, Typ, Stromkreis) und wie verklemmt wird (L, N, PE, Schaltdraht, Korrespondierende) als kleines Klemmenbild im Stil des Schaltbilds
- [ ] Belegung prüfen: Leitungen und Adern je Dose zählen; Hinweis (ignorierbar), wenn es eng wird, z. B. mehr als 4 Leitungen in einer normalen Dose, mehr als 3 mit Aktor, oder viele Klemmen; Vorschlag: tiefe Dose oder Abzweigdose
- [ ] Einstellung Verdrahtung (Menü → Vorgaben): „nur in Schalterdosen“ (Standard) · „Abzweigdosen vorschlagen“ · „Abzweigdosen frei verwenden“
- [ ] Vorschläge im Plan (Schalter im Menü „Ebenen“): gestrichelte Punkte, wo eine Abzweigdose sinnvoll ist, z. B. überfüllte Schalterdose, Verzweigung zu mehreren Leuchten in verschiedene Richtungen, langer Rückweg Schalter → Leuchte, der sich mit Abzweigdose deutlich verkürzt; Antippen zeigt den Grund und die Ersparnis (m Leitung, Leitungen je Dose), „Übernehmen“ setzt eine echte Abzweigdose und führt die Schaltung darüber
- [ ] Abzweigdose als Element (Katalog, Suchwörter „Verteilerdose, Klemmdose“), manuell setzbar, Schaltung zuordnen; Hinweis, dass Abzweigdosen zugänglich bleiben müssen (nicht zuputzen/zutapezieren)
- [ ] Hängt am Leitungsverlauf aus 0.7.4 (eigene Wege, Reihenfolge der Leuchten)

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
