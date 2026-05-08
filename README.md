# Spanisch_EF_a_tope
# a_tope — Spanisch lernen 🌙

Eine Lern-App für den Spanischunterricht, begleitend zum Lehrwerk **a_tope nueva edición** (Cornelsen). Konzipiert für Schüler\*innen der Einführungsphase (EF) am Gymnasium NRW, Spanisch neu einsetzend.

## Wozu diese App?

Duolingo ist motivierend — aber der Wortschatz passt nicht zum Unterricht und Grammatikübungen fehlen. Diese App schließt genau diese Lücke: gleiche Spielmechanik, aber mit dem Vokabular und der Grammatik aus *a_tope*, strukturiert nach Unidades.

## Features
### Lerninhalte
- **Vokabeln** aus allen 9 Unidades (¡Hablamos! bis Unidad 8) — über 270 Wörter
- **Grammatikübungen** zu 11 Themen: ser/estar, gustar, Imperativ, Reflexivverben, Komparativ, Indefinido (regulär + unregelmäßig), Imperfecto, Futur, Konditional
- **Konjugationsübungen** in allen 5 Tempora als Lückentext
- **KI-generierte Dialoge** (7 Szenarien aus dem Buch) mit Feedback durch die Anthropic API

### Adaptives Lernen
- **Spaced Repetition**: Wörter mit Fehlern kommen häufiger wieder
- **Fehlerprofil**: Die App merkt sich pro Wort und Grammatikthema, wie oft richtig/falsch
- **Gewichtete Übungsauswahl**: Schwächen werden automatisch öfter geübt
- **Wochenbericht** im Profil-Tab mit Trefferquoten und härtesten Wörtern
- **KI-Dialoge** nutzen das persönliche Fehlerprofil für gezielte Übungen

### Motivation
- **Streak** + **Tagesziel** (Duolingo-Mechanik)
- **XP-System** mit Level-Progression
- **21 Abzeichen** für Streak, XP, Unidades, Modi
- **Abzeichen-Toast** mit Animation
- **Konfetti** bei 100% oder erreichtem Tagesziel
- **Wort des Tages** (täglich wechselnd, direkt übbar)
- **Schnell-Runde** (3 Fragen, unter 3 Minuten)
- **Charakterfeedback** mit abwechselnden Reaktionen

### Design & Technik
- Dunkles OLED-Design (akkuschonend auf modernen Smartphones)
- Optimiert für Smartphone und iPad
- Touch-Targets ≥ 52px, Swipe-Gesten, Haptic Feedback
- Stadtsilhouette (Madrid, Barcelona, Lima, Buenos Aires, México) im Willkommensbildschirm
- **Komplett offline** für alle eingebauten Übungen
- KI-Dialoge benötigen eine Internetverbindung (optional)

### Datenschutz
- **Kein Konto**, keine E-Mail, keine Registrierung
- **Anonymes Login** per selbstgewähltem Spitznamen
- **Keine Datenübertragung**: Alle Lernfortschritte werden ausschließlich lokal im Browser gespeichert (`localStorage`)
- GitHub empfängt nur standard HTTP-Zugriffslogs (IP, Zeitstempel) — keine Lerndaten
- DSGVO-konform für den Schulbetrieb

## Nutzung

Die App läuft direkt im Browser — keine Installation nötig.

**→ [App öffnen](https://DEINNAME.github.io/atope-spanisch/)**

Auf dem Smartphone als Lesezeichen auf dem Homescreen speichern:
- **iPhone/iPad**: Teilen-Symbol → „Zum Home-Bildschirm"
- **Android**: Dreipunkt-Menü → „Zum Startbildschirm hinzufügen"

## Technischer Aufbau

Die gesamte App besteht aus einer einzigen HTML-Datei (`index.html`) ohne externe Abhängigkeiten außer zwei Google Fonts. Kein Framework, kein Build-Prozess, kein Server.

| Komponente | Technik |
|---|---|
| Vokabel- & Grammatikdaten | Statisches JS-Array (aus dem Buch) |
| Adaptives Lernen | SM-2-inspiriertes Gewichtungssystem, `localStorage` |
| KI-Dialoge | Anthropic Claude API (`claude-sonnet-4-20250514`) |
| Konfetti | Canvas API |
| Haptic Feedback | Web Vibration API |
| Fortschritt | `localStorage` (gerätlokal, kein Sync) |

---

## Für Lehrkräfte

### Einsatz im Unterricht
- Als freiwillige Hausaufgaben-Ergänzung
- Zur Vorbereitung auf Vokabeltests
- Für die tägliche 5-Minuten-Wiederholung
- Schüler\*innen müssen sich **nicht** mit echtem Namen anmelden

### Wortschatz anpassen
Der Wortschatz liegt als JavaScript-Array im `<script>`-Bereich der Datei. Neue Vokabeln können einfach im Format `{es:'palabra', de:'Wort'}` ergänzt werden.

### KI-Dialoge ohne Internet
Alle 7 Dialog-Szenarien haben eingebaute Offline-Fallbacks. Die App funktioniert vollständig ohne Internetverbindung — die KI ist eine optionale Erweiterung.


## Inhaltsübersicht nach Unidad

| Unidad | Thema | Grammatik |
|---|---|---|
| ¡Hablamos! | Begrüßung & Vorstellung | — |
| Unidad 1 | Alltag & Schule | Presente regulär, ser, Verneinung |
| Unidad 2 | Familie & Wohnen | tener, Adjektiv-Angleichung, Possessivbegleiter |
| Unidad 3 | Freizeit, Hobbys & Kleidung | gustar/encantar, tampoco, indir. Objektpronomen |
| Unidad 4 | Tagesablauf & Uhrzeit | Reflexivverben, Imperativ tú, ir a + Inf. |
| Unidad 5 | Stadt & Orientierung | Komparativ/Superlativ, direkte Objektpronomen |
| Unidad 6 | Reisen & Vergangenheit | Indefinido regulär & unregelmäßig, hace/desde |
| Unidad 7 | Berufe & Zukunft | Konditional, indirekte Rede, se-Konstruktionen |
| Unidad 8 | Umwelt & Spanien | Imperfecto, Indefinido vs. Imperfecto, Adverbien -mente |

## Lizenz & Nutzung

Diese App ist für den unterrichtlichen Einsatz an Schulen entwickelt. Der Vokabular- und Grammatikinhalt basiert auf *a_tope nueva edición* (Cornelsen Verlag). Die App selbst — Code, Design, adaptive Lernlogik — darf für schulische Zwecke frei genutzt und angepasst werden.

*Erstellt mit [Claude](https://claude.ai) · Cornelsen-Lehrwerk a_tope nueva edición (2017)*
