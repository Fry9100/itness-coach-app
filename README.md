# Fitness-Coach (iOS Web-App)

Eine einzelne, self-contained `index.html` – kein Server, kein Build-Schritt nötig.
Läuft offline und lässt sich auf dem iPhone wie eine echte App benutzen.

## Auf dem iPhone installieren

1. `index.html` auf dem iPhone öffnen (z. B. per AirDrop, iCloud Drive/Dateien-App,
   oder über GitHub Pages, falls das Repo gehostet wird) – in **Safari** öffnen.
2. Teilen-Symbol (Viereck mit Pfeil) antippen.
3. **"Zum Home-Bildschirm"** wählen.
4. Ab jetzt öffnet sich die App per Icon im Vollbild, ganz ohne Safari-Leiste.

Alle Eingaben (Profil, Tages-Logs) werden lokal auf dem Gerät gespeichert (`localStorage`,
mit Fallback auf einen In-Memory-Speicher falls der Browser-Kontext Storage blockiert) und
bleiben zwischen App-Starts erhalten.

## Wie die App funktioniert

Kein Auswählen nötig – die App sagt an, was an einem Tag zu tun ist, wie ein persönlicher
Trainer:

- **Heute-Tab:** Wochentag-Leiste oben (Mo–So der aktuellen Woche) zum Ansehen/Nachtragen
  einzelner Tage. Für den gewählten Tag: Rad-km/Höhenmeter eintragen, Ruhetag/Reisetag
  markieren, und die App zeigt genau die fällige Krafteinheit (Übungen, Sätze, Wiederholungen,
  geschätzte Studiozeit) sowie den passenden Ernährungsplan mit portionsgenauen Mengen.
- **Adaptive Planung ohne Kalenderbindung:** Die App zählt tatsächlich absolvierte Einheiten,
  nicht Kalendertage. Einheit A/B wechseln sich ab; verpasst/pausiert man einen Tag, rutscht
  die fällige Einheit automatisch auf den nächsten passenden Tag (kein Nachholen mit zwei
  Einheiten am selben Tag). Nach je 3 absolvierten Einheiten steigt die Woche im
  4-Wochen-Progressionsblock (Sätze/Wdh./Intensität).
- **Reagiert auf Radfahren:** Trägt man Kilometer/Höhenmeter ein, passt sich sowohl das
  Kalorien-/Makroziel als auch die Trainingsempfehlung für diesen Tag automatisch an – bei
  einer großen Ausfahrt (≥70 km oder ≥800 Hm) wird bewusst kein zusätzliches Krafttraining
  vorgeschlagen (Erholung hat Vorrang), und Portionsgrößen (Reis/Kartoffeln) skalieren mit dem
  errechneten Kohlenhydratbedarf.
- **Übungen-Tab:** Nachschlagewerk mit Zielmuskel-Piktogramm, Ausführung, häufigem Fehler und
  einem Link zu einer YouTube-Suche für Video-Anleitungen (bewusst eine Suche statt einer fest
  verlinkten Video-ID, damit der Link nie ins Leere läuft).
- **Mehr-Tab:** Profil (Gewicht/Größe/Alter/Ziel-Einheiten pro Woche/Kaloriendefizit, wird
  sofort gespeichert und rechnet live neu), Ernährungsprinzipien, ESN-Supplement-Empfehlungen
  (Whey, Kreatin) mit Dosierung/Timing, und ein Reset für alle gespeicherten Daten.

## Getroffene Annahmen (noch nicht final bestätigt)

- Alter: 30 Jahre
- Ziel: 3 Krafteinheiten/Woche, 300 kcal Tagesdefizit

Alle vier Werte lassen sich im Tab "Mehr" direkt anpassen. Die Ernährung ist vegetarisch
(kein Fleisch, kein Fisch – Eier/Milchprodukte sind enthalten). Bei zusätzlichen
Einschränkungen (vegan/laktosefrei) bitte kurz Bescheid geben – Ernährungsplan und
Supplement-Empfehlung (z. B. ESN Ultrapure Whey Isolate statt Designer Whey bei
Laktoseproblemen) lassen sich leicht anpassen.
