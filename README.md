# Rechtschreib-Labor – Wörter untersuchen & Rechtschreibstrategien anwenden

Ein Lernspiel der Reihe **Förderfreude Games** für die Klassen 2–4, für Förderunterricht und Sprachförderung.
Kinder arbeiten als Wortforscher:innen in einem freundlichen Labor: Sie untersuchen Wörter und wenden Rechtschreibstrategien an, statt nur „richtig oder falsch“ zu raten.

## Das Spiel
- **Eine Datei:** `index.html` (HTML, CSS und JavaScript, alle Grafiken als eigene SVGs).
- Keine externen Dateien, keine Schriften, keine Cookies, kein Tracking, kein Speichern im Browser.
- Läuft direkt per Doppelklick oder auf Netlify/GitHub Pages (statische Seite, kein Build nötig).

### Die sieben Stationen im Labor
1. **Verlängerungsstation** – Auslautverhärtung (d/t, g/k, b/p): Wort verlängern (Hund → Hunde), dann den Buchstaben wählen.
2. **Wortfamilien-Analyse** – ä/äu über verwandte Wörter (Häuser → Haus).
3. **Silben-Mikroskop** – Silben zusammensetzen, Silbenende finden, Schreibweise mit Doppelkonsonant wählen, Silbenhälften verbinden.
4. **Wortbaustoffe** – Wörter aus Vorsilbe, Wortstamm und Endung bauen oder zerlegen.
5. **Fehlerdetektor** – Fehler im Satz finden, Strategie wählen, anwenden und verbessern.
6. **Strategiezentrale** – Zu einer unsicheren Stelle die passende Strategie wählen und anwenden.
7. **Das große Rechtschreib-Experiment** – alle Aufgabentypen gemischt (nie derselbe Typ zweimal hintereinander).

Es werden genau vier Strategien trainiert: **Verlängern, Ableiten, Silben untersuchen, Wortbausteine erkennen.**
Jede Runde hat **acht Aufgaben** (ein Reagenzglas füllt sich je gelöster Aufgabe) und drei Stufen (leicht, mittel, schwer; die Stufen unterscheiden sich in Hilfen und Wortschatz, nicht nur in der Zahl der Antworten).
Es gibt keine Zeit, keine Punkte, keine Leben und kein Game Over. Bei einer falschen Antwort bleibt der Fortschritt erhalten, es erscheint ein kurzer freundlicher Hinweis und die Lösung wird nicht verraten. Der Knopf „Tipp“ gibt einen zusätzlichen Hinweis.

### Bedienung
Maus, Touch und Tastatur (Tab, Enter, Leertaste). Alle Aufgaben lassen sich durch Antippen lösen. Zielgrößen mindestens 44 px, WCAG-AA-Kontraste, sichtbarer Fokus, ARIA-Beschriftungen, `prefers-reduced-motion` wird beachtet.

### Sprachausgabe
Die Sprachausgabe nutzt `SpeechSynthesis` (de-DE) des Browsers und startet **nur nach Antippen eines Lautsprechers**. Sie ist nie nötig, um eine Aufgabe zu lösen. Falsche Schreibungen werden nie vorgelesen. Gibt es keine deutsche Stimme, wird der Ton ausgeblendet. „Ton testen“ steht im Hilfe-Dialog.

## Aufgaben und Qualitätssicherung
Alle Wörter, Verlängerungen, verwandten Wörter, Silbentrennungen, Wortbausteine und Fehlersätze sind **einzeln festgelegt** (ca. 330 Datensätze) und stehen im Quelltext im Datenblock. Nichts wird automatisch abgeleitet.
Jede Aufgabe wird vor der Anzeige unabhängig geprüft (genau eine Lösung, keine zweite Kartenreihenfolge, kein Hinweis verrät die Lösung); jede Runde wird vor dem Start geplant und geprüft. Siehe Ordner `pruefung/`.

## Ordner
| Pfad | Inhalt |
|---|---|
| `index.html` | das Spiel |
| `arbeitsblaetter/` | Teilnehmerübersicht (A4 quer, 30 × 10) und zwei Arbeitsblätter (HTML + PDF), unabhängig vom Spiel einsetzbar; keine Lösungsblätter |
| `pruefung/` | Materialübersicht (HTML, CSV, PDF), fachliche Checkliste, Aufgabenzahlen und Strategien, Testbericht |

## Lokal starten
`index.html` im Browser öffnen. Für Tests mit Hilfsfunktionen: `index.html#qa`.

## Veröffentlichen
1. Repository auf GitHub anlegen und diese Dateien hochladen.
2. Auf Netlify „Add new site → Import from Git“ wählen; Build-Befehl leer lassen, Publish-Verzeichnis `/`.
3. Das Netlify-Badge liegt unten rechts; der Bereich ist über die Variable `--badge` freigehalten.

## Browser und bekannte Grenzen
Aktuelle Versionen von Chrome, Edge, Firefox und Safari; getestet wurde in Chromium (Desktop- und Touch-Emulation, 360×640 bis 2560×1440). Die Sprachausgabe hängt von den Stimmen des Geräts ab. Beim Silben- und Bausteinschnitt sind die Wörter auf höchstens 7 Buchstaben begrenzt (Touch-Zielgröße).

Eigene Illustrationen und Texte. © Förderfreude Games.
