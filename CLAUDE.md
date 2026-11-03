# tagebuch

Nur `index.html` (Schloss + Anzeige) und `daten.enc` (AES-256-GCM, PBKDF2-SHA256 600k).
Klartext und Werkzeuge liegen außerhalb: `~/Skripte/tagebuch/`. Nie Klartext hier einchecken.

## Bekannte Fallen
- `index.html` ist zugleich Vorlage der PC-Fassung (`~/Skripte/tagebuch/lokal.py` ersetzt Teile per Text) →
  nach Änderungen `lokal.py` laufen lassen und prüfen, dass die Ersetzungen noch greifen.
- Einträge ohne Anrede („du/dein“); `pruefen.py` warnt im `abendlauf.log`. Stärken ohne „er/sie“; `staerken.py` verwirft sie.
- Vorher→Nachher wird aus den Texten gelesen → nur mit Einheit aus `EINHEITEN`; neue Einheit dort ergänzen,
  nicht die Erkennung lockern (sonst „0,20 → 0,18 senken“).
- Tage ohne Beiträge bekommen eine Datei mit `grund` (abendlauf.sh `leerer_tag`), die Seite zeigt sie im Verlauf.
