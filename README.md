# Judo Grün-Weiß 90 Dresden – Website

Statische Website ohne CMS, Datenbank oder Plugins. Keine Updates nötig.

## Dateien

| Datei | Inhalt |
|---|---|
| `index.html` | Die komplette Seite (Training, Beiträge, Anfahrt, Aktuelles, Partner, Kontakt) |
| `style.css` | Design; Farben ganz oben unter `:root` |
| `impressum.html`, `datenschutz.html` | Rechtliches |
| `fonts/` | Schriften, lokal gehostet (kein Google-Fonts-Abruf, DSGVO-freundlich) |
| `img/` | Bilder (vor dem Hochladen auf max. ca. 1800 px Breite verkleinern) |
| `_original/` | Originalbilder (alte Seite + Instagram in voller Größe), wird nicht veröffentlicht |

## Typische Änderungen

- **Trainingszeiten:** im Abschnitt `TRAINING` bei jedem Balken `data-start`/`data-end` und den Text im `<small>` ändern. Balken und die Anzeige „Nächstes Training“ passen sich automatisch an.
- **Beiträge:** in `index.html` die Zeile suchen und die Zahl ändern.
- **Neue Meldung** (z. B. nach einem Instagram-Post): Bild nach `img/news/` legen (ca. 900 px breit), im Abschnitt `AKTUELLES` einen `<article class="post">`-Block kopieren, oben einfügen und Link, Bild, Datum, Überschrift und Text anpassen. Den untersten Block löschen, damit es 6 bleiben.
- **Neuer Sponsor:** Logo nach `img/` legen, im Abschnitt `SPONSOREN` einen `<a>`-Block kopieren.

## Lokal ansehen

```bash
python3 -m http.server 8420
```

Dann http://localhost:8420 öffnen.

## Veröffentlichen

Empfehlung: Ordner in ein GitHub-Repository legen und mit **Cloudflare Pages** oder **Netlify** verbinden (kostenlos).
Jede Änderung, die gepusht wird, ist nach ca. 1 Minute online. Die Domain `gw-dd-judo.de` wird dort per DNS-Eintrag verbunden.
`_original/` und `README.md` vorher per `.gitignore` bzw. Build-Einstellung ausschließen oder löschen.

## Vor dem Livegang offen

- [ ] Impressum: Vereinsanschrift, Registergericht und VR-Nummer eintragen
- [ ] Datenschutz: Hoster eintragen, Text prüfen lassen
- [ ] Gürtelreihenfolge im Abschnitt „Dein Weg“ mit der aktuellen DJB-Kyu-Ordnung abgleichen
- [ ] Trainingszeiten, Beiträge und Ansprechpartner auf Aktualität prüfen
- [ ] Einverständnis für die Fotos klären (stammen von @judodresden, zeigen teils Minderjährige); Hero-Bild ist noch von 2023
- [ ] Optional: eigene Kontaktadresse wie `judo@gw-dd-judo.de` mit Weiterleitung, statt privater Adressen
