# Fotoeffekt-Simulation – Spezifikation

**Umsetzung:** `index.html` im selben Ordner (erste Fassung 28.10.2026).
Direkt zu einem Schritt springen: `index.html#schritt=5`. Lehrermodus:
Strg + Umschalt + L oder dauerhaft der Schalter in Zeile 6 der `index.html`.

Stand: 05.11.2026 (Inhalt vom 28.10.2026, Aussehen angeglichen, siehe unten) · Zielgruppe: kommender
13er-Kurs (jetzt 12er, Abitur 2028, Moodle-Kurs 644, Schulbuch **Dorn-Bader**) · Lernpaket: `Fotoeffekt_SCORM.zip`.

## Rahmen
- **Eine HTML-Datei** mit integriertem CSS und JavaScript, offline lauffähig
  (Laptop, Beamer, iPad), deutsch, modernes Aussehen.
- Lernprogramm mit **mehreren Seiten**, das Schritt für Schritt durch den Versuch
  führt. Arbeitsaufträge fürs **Heft**, dazu ein **Selbstcheck** pro Seite
  (Auswahlfragen bzw. Zahlenantworten mit Toleranz, sofortige Rückmeldung).
- Begriffe/Formelzeichen wie Dorn-Bader: **Fotoeffekt, Fotokathode, Ringanode,
  Gegenspannung *U*<sub>g</sub>, Fotostrom *I*<sub>Ph</sub>, Austrittsarbeit
  *W*<sub>A</sub>, Grenzfrequenz *f*<sub>G</sub>**, *E*<sub>kin</sub> = h·f − W<sub>A</sub>.
- Zustand (Seite, Einstellungen, Messwerte) wird im Browser gespeichert.
- **Hell/Dunkel-Schalter** oben rechts (Mond/Sonne). Beim ersten Start gilt die
  Einstellung des Geräts, danach die eigene Wahl (im Browser gespeichert).
  Diagrammfarben je Design eigens geprüft; die Szene ist in beiden Designs dunkel.
- **Lehrermodus** wie im Skill `lernsimulation` (füllt alles aus, zeigt W<sub>A</sub>, E<sub>kin,max</sub>, Grenzwerte).

## Aufbau der Szene (wie Dorn-Bader B1)
- Licht/Photonen von **links nach rechts**, **durch die Ringanode hindurch** auf
  die **Fotokathode rechts** (nach links gewölbt), Vakuum-Glaskolben.
- Elektronen fliegen von **rechts nach links** zur Ringanode; im Gegenfeld
  werden sie abgebremst und kehren um, wenn ihre Energie nicht reicht;
  bei beschleunigender Spannung werden sie schneller.
- Schaltung: Amperemeter *I*<sub>Ph</sub>, regelbare Spannungsquelle *U*<sub>g</sub>, Erdung.
- Optional: nur die schnellsten Elektronen zeigen.

## Bedienelemente
- **Lichtquelle**
  - Entdeckungsseiten: Wellenlänge frei einstellbar (ca. 200–800 nm, inkl. UV)
  - Messseite: **Hg-Lampe mit Filter**: gelb 5,19 · grün 5,49 · türkis 6,08 ·
    blau 6,88 · violett 7,41 (· UV 8,21) × 10<sup>14</sup> Hz
  - **Intensität** 0–100 % (ändert nur die Anzahl der Photonen)
- **Kathodenmaterial:** Cäsium, Kalium, Natrium, Wolfram-Cäsium, AgCsO, Zink
- **Gegenspannung** auch negativ (beschleunigend); grober Regler **plus
  Feinknöpfe ±0,01 V**, Pfeiltasten, Zahleneingabe; Anzeige mit 2 Nachkommastellen.
- Messgeräte: *U*<sub>g</sub> in V, *I*<sub>Ph</sub> in µA (3 Nachkommastellen).

## Physikmodell
- E<sub>Ph</sub> = h·f; Elektronen nur bei h·f > W<sub>A</sub>; Energie gleichverteilt
  zwischen 0 und E<sub>kin,max</sub> = h·f − W<sub>A</sub>.
- Fotostrom ∝ Intensität; bei Gegenspannung linear abnehmend und **null** ab dem
  0,01-V-Wert, der E<sub>kin,max</sub>/e am nächsten liegt.
- Elektronen treten in verschiedene Richtungen aus und fliegen ohne Spannung
  **geradeaus**: nur ein Teil (65 %) trifft die Ringanode, der Rest fliegt durch
  den Ring gegen die Glaswand. Beschleunigende Spannung erhöht den Anteil bis
  zur Sättigung (alle ab −1 V). Der Fotostrom folgt demselben Modell.
- Start mit Intensität 0 % (Lampe aus).
- **Exakte Werte** (kein Messrauschen). Austrittsarbeiten so gewählt, dass die
  Lösungen von RAAbits und Fokus (±0,01 V) stimmen:

| Material | W<sub>A</sub> |
|---|---|
| AgCsO | 1,14 eV |
| Wolfram-Cäsium | 1,41 eV |
| Kalium | 1,81 eV |
| Cäsium | 1,94 eV |
| Natrium | 2,28 eV |
| Zink | 4,27 eV |

## Seiten des Lernprogramms
Photonen kommen erst ab Schritt 5 vor (sie sind das Ergebnis des Versuchs):
Schritt 1–4 zeigen das Licht als **Welle**, deren Amplitude mit der Intensität
wächst; Texte und Selbstchecks dort nur beobachtend, ohne „Photon“. Ab
Schritt 6 standardmäßig Photonendarstellung. Schrittnamen in der Kopfzeile:
Aufbau · Intensität · Wellenlänge · Material · Welle oder Teilchen? ·
Gegenfeldmethode · Diagramm · Deutung.

1. **Der Versuchsaufbau** – Bauteile kennenlernen
2. **Intensität** – Strom und Elektronengeschwindigkeit bei mehr Licht
3. **Wellenlänge** – Grenzwellenlänge finden (Natrium)
4. **Kathodenmaterial** – Grenzfrequenzen vergleichen
5. **Welle oder Teilchen?** – Erwartung nach dem Wellenmodell (Intensität =
   Amplitude) vs. Beobachtung; Einsteins Deutung (1905), E = h·f,
   E<sub>kin,max</sub> = h·f − W<sub>A</sub>; Umschalter Welle/Photonen
6. **Gegenfeldmethode** – Messreihe mit Hg-Linien; **Messwerte speichern**
   in eine sichtbare Tabelle (Material, Farbe, λ, f, Intensität, U<sub>g</sub>,
   I<sub>Ph</sub>; E<sub>kin</sub>-Spalte optional zuschaltbar). Die Tabelle muss
   sich gut von Hand auf Millimeterpapier übertragen lassen.
7. **Diagramm** – Tabelle ins Heft, E<sub>kin</sub> berechnen, Achsen selbst
   wählen (lineare Darstellung finden), Millimeterpapier, Ausgleichsgeraden,
   Steigung → h. Diagramm in der Simulation mit frei wählbaren Achsen zur Kontrolle.
8. **Deutung: Grenzfrequenz und Austrittsarbeit** – ohne Messwerttabelle; festes
   E<sub>kin</sub>-f-Diagramm mit den eigenen Ausgleichsgeraden (bis zu den Achsen
   verlängert), zusätzlich ideale „theoretische Geraden“ für beliebige Materialien
   (gestrichelt). Schalter „Grenzfrequenz und Austrittsarbeit anzeigen“ markiert die
   Schnittpunkte und zeigt die Werte (Standard: aus). Rückbezug: λ<sub>G</sub> aus
   f<sub>G</sub> mit Schritt 3/4 vergleichen.
9. **Ausblick (Zusatz)** – zählt nicht zum Fortschritt, kein Selbstcheck, auch
   für den Beamer gedacht. Zeitleiste mit Kennzeichnung Experiment/Theorie
   (Hertz 1887, Hallwachs 1888, Thomson 1899, Planck 1900, Lenard 1902,
   Einstein 1905, Millikan 1916 als Pointe: dieselbe Auswertung wie Schritt 6–8,
   Nobelpreise 1921/1923) und Anwendungen äußerer vs. innerer Fotoeffekt.

## Bewusst nicht enthalten
- I-U-Kennlinie als eigenes Thema · Messrauschen · Einstiegsarbeitsblatt
  (bleibt vorerst unverändert)

## Herkunft der Anforderungen
- Favorit: RAAbits-Simulation (`photoeffekt.exe`, nur Windows) und ihr
  Arbeitsblatt; Fokus-Arbeitsblatt nutzt dieselben Werte.
- Gesichtet: Dorn-Bader B1, LEIFI/Fendt, PhET (Java), Physics-Zone.
- Arbeitsblatt „Photoeffekt Einstieg“ (`02b`): freie Wellenlänge, Intensität,
  sichtbare Elektronengeschwindigkeit, Nullstrom-Methode.
- Notiert für später (Einstiegsblatt): f = λ/c → f = c/λ; „Plank“ → Planck;
  Lichtquanten-Hypothese stammt von Einstein, nicht von Planck.

## Äußere Angleichung an den Skill `lernsimulation` (05.11.2026)
Die Simulation soll aussehen, als wäre sie mit dem Skill entstanden. Wortlaut, Aufgaben und Physik sind unverändert
(maschinell verglichen). Einzige neue Textzeile: „Die Tabelle steht unter diesen Feldern.“ (Feld „Fotostrom“, ab Schritt 6).

- **Übernommen:** Fußzeile, MIT-Lizenz (`LICENSE`, Kommentar in der Datei), CSS der Vorlage samt Kompaktmodus für
  Laptops, Kante um die Szene, Szene füllt die Höhe (mindestens 320 px), Spalten bündig, Kopfzeile ab 1366 px einzeilig,
  LCD ragt nie aus dem Kasten, Knöpfe unter der Szene in schmalen Fenstern, Anleitung beginnt beim Schrittwechsel oben.
- **Formeln:** KaTeX eingebettet, waagerechte Bruchstriche, Formelzeichen auch in Feldern, Tabellenköpfen und Szene.
- **Zeichnung:** Hinweisstriche enden auf Fotokathode und Ringanode, Leitung geschlossen, langer Strich der
  Spannungsquelle immer am Pluspol, Namen im Diagramm überlappen sich nicht mehr.
- **Bewusst geblieben:** vier statt zwei Felder (der Versuch braucht alle gleichzeitig), Diagramm auf eigener Seite in
  Schritt 7 und 8, Umfang (34 Aufträge, 20 Fragen).

## Korrekturen nach dem Test (06.11.2026)
- **Lehrermodus wie im Skill:** Schalter in Zeile 6, Strg + Umschalt + L, füllt in jedem Schritt alles aus (auch 12 Messwerte
  und das Diagramm), speichert mit dem Kürzel nichts. `#lehrer` in der Adresse entfällt.
- **„Sofort“:** Beim Aufdrehen ist das Lichtbündel sofort gefüllt und das erste Elektron tritt sofort aus (`seedBeam`).
  Vorher brauchte es 1,1 bis 2,2 s, weil die Photonen erst zur Kathode flogen. Beim Ausschalten ist kein Licht mehr unterwegs.
- **Speichern:** Bei ausgeschalteter Lampe und unterhalb der Grenzfrequenz (Natrium gelb und grün, Zink immer) entsteht kein
  Messwert, die Meldung nennt den Grund. Die Nullen verfälschten vorher die Gerade: Steigung 0,93 · h und W_A = 2,07 eV bei
  Natrium. Liegt die Spannung mehr als 0,02 V über der Grenzspannung, wird gespeichert, gewarnt und rot markiert.
- **Anzeige bei schwachem Licht:** Das Amperemeter zeigt bis zur Grenzspannung mindestens 0,001 µA. Vorher sprang es bei 1 %
  Intensität schon bei 0,87 V statt 0,91 V auf null, die Grenzspannung schien also von der Intensität abzuhängen.
- **Selbstcheck:** Getippte, ungeprüfte Zahlen und das gewählte Material bleiben, wenn eine andere Frage beantwortet wird. Die
  Rückmeldung gilt immer für die letzte Antwort. Ein einmal erreichter Haken bleibt.
- **Moodle:** Eigener Browserspeicher je Schüler, beim Öffnen gilt der neuere Stand, beim Schließen wird gesichert. Messwerte
  liegen platzsparend im Stand: 129 statt 30 passen in `suspend_data`. Ältere Stände lassen sich weiter lesen.
- **Diagramm:** Blendet man ein Material aus, behalten die anderen ihre Farbe.

## Lernpaket
- Abgenommen und ersetzt am 06.11.2026: Kurs 330, cmid 36659 (`moodle replace-file`, die Aktivität und die Stände der Schüler bleiben).
- Nach weiteren Änderungen das Paket erst nach der Abnahme neu bauen (`paket.py`) und ebenso ersetzen.
