# OCTA · NC/tmp‑Achsen‑Importer · 9×9 · 81‑Matrix

OCTA ist ein 9×9‑Matrix‑Launcher, der alle Achsen (tmp‑Files) aus dem
NC/tmp‑Pool automatisch erkennt, kopiert und in die eigene Struktur einbindet.

Damit wird OCTA zu einem selbstversorgenden NC‑Modul:
Es lädt alle relevanten tmp‑Achsen ohne manuelle Arbeit.

──────────────────────────────────────────────
## 🔹 Zweck

- Alle NC/tmp‑Achsen automatisch übernehmen
- Alle tmp‑Parameter (DE/TR/EN, X, Q, C, room‑Achsen) einlesen
- WHIRL.json, REAL.json, Quadrant.json automatisch füttern
- 9×9 OCTA‑Matrix vollständig befüllen
- 81 Felder automatisch generieren
- Keine manuelle Pflege notwendig

──────────────────────────────────────────────
## 🔹 Import‑Quelle (NC/tmp Pool)

OCTA importiert folgende Achsen aus dem NC/tmp‑Pool:

- `lang.DE.json`
- `lang.EN.json`
- `lang.TR.json`
- `mode.X.json`
- `user.Q.json`
- `value.C.json`
- `CR.json`
- `X.room.IN.json`
- `X.room.CORE.json`
- `X.room.OUT.json`

Alle Dateien werden automatisch erkannt und übernommen.

──────────────────────────────────────────────
## 🔹 Auto‑Copy Mechanismus

Beim Start liest OCTA:

1. den Ordner `NC/tmp/`
2. alle `.json`‑Achsen
3. kopiert sie in den eigenen Achsen‑Pool
4. aktualisiert WHIRL.json (81 Felder)
5. aktualisiert REAL.json (Routing)
6. aktualisiert Quadrant.json (4× Quadranten)
7. aktualisiert OCTA.json (9×9 Matrix)

──────────────────────────────────────────────
## 🔹 WHIRL‑Integration

WHIRL.json wird automatisch mit allen tmp‑Achsen gefüllt:

- 81 Felder
- jede Achse wird mehrfach zyklisch eingebunden
- vollständige Rotation
- vollständige RESPO‑Kompatibilität

──────────────────────────────────────────────
## 🔹 REAL‑Integration

REAL.json erzeugt:

- 9×9 Routing‑Matrix
- direkte Achsen‑Verbindung
- automatische RESPO‑Zuweisung

──────────────────────────────────────────────
## 🔹 Quadrant‑Integration

Quadrant.json erzeugt:

- 4 Quadranten
- jede Achse wird einem Quadranten zugeordnet
- NC‑Drift‑Kompatibilität

──────────────────────────────────────────────
## 🔹 Dateien in diesem Repository

- `index.html` – OCTA‑Launcher
- `WHIRL.json` – 81‑Felder‑Rotation
- `REAL.json` – Routing‑Matrix
- `OCTA.json` – 9×9 Matrix
- `Quadrant.json` – Quadranten‑Routing
- `README.md` – diese Dokumentation

──────────────────────────────────────────────
## 🔹 Startpunkt

OCTA kann direkt über `index.html` gestartet werden.
Alle tmp‑Achsen werden automatisch geladen.
