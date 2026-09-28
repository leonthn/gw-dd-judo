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

Die Seite läuft über **GitHub Pages**: https://leonthn.github.io/gw-dd-judo/
Repository: https://github.com/leonthn/gw-dd-judo

Änderung online stellen:

```bash
git add -A && git commit -m "Beschreibung der Änderung" && git push
```

Nach ca. 1 Minute ist die Änderung live. Alternativ lassen sich Dateien auch direkt auf github.com bearbeiten („Edit“-Stift).

### Umzug auf gw-dd-judo.de (wenn es so weit ist)

1. In `index.html` die Zeile `<meta name="robots" content="noindex">` löschen.
2. Auf GitHub: Settings → Pages → Custom domain `gw-dd-judo.de` eintragen, „Enforce HTTPS“ aktivieren.
3. Beim Domain-Anbieter die DNS-Einträge setzen: A-Records auf `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153` und CNAME `www` → `leonthn.github.io`.
4. Den Hoster in `datenschutz.html` eintragen (GitHub Inc., USA).

## Vor dem Livegang offen

- [ ] Impressum: Vereinsanschrift, Registergericht und VR-Nummer eintragen
- [ ] Datenschutz: Hoster eintragen, Text prüfen lassen
- [ ] Gürtelreihenfolge im Abschnitt „Dein Weg“ mit der aktuellen DJB-Kyu-Ordnung abgleichen
- [ ] Trainingszeiten, Beiträge und Ansprechpartner auf Aktualität prüfen
- [ ] Einverständnis für die Fotos klären (stammen von @judodresden, zeigen teils Minderjährige); Hero-Bild ist noch von 2023
- [ ] Optional: eigene Kontaktadresse wie `judo@gw-dd-judo.de` mit Weiterleitung, statt privater Adressen
