# HIIT Trainer

Een persoonlijke HIIT-trainingsapp die je hartslagband (Bluetooth) uitleest en
Spotify op je telefoon aanstuurt. Werkt als "tegel" (PWA) op je Android-scherm.

## Wat de app doet

1. **Setup** — koppel je hartslagband (verplicht). Spotify is **optioneel**:
   zonder koppeling train je gewoon zonder muziek.
2. **Onderdeel 1 — 4 pieken** — per piek speelt je werk-playlist (bij piek 1
   geshuffled, bij de volgende pieken springt de app naar een ander nummer
   voor variatie). Zodra je hartslag op/boven 130 komt hoor je "De timer
   start!" en moet je dat 1 minuut *volhouden* (de timer pauzeert zodra je
   hartslag onder 130 zakt). Bij 45/30/15 seconden wordt dit omgeroepen, de
   laatste 5 seconden worden afgeteld.
3. **Herstel na elke piek** — rustgevende muziek start meteen. Hartslag moet
   naar 100 of lager. Na 30 seconden start automatisch een ademhalingsoefening
   (4 tellen in, 6 tellen uit, 1 tel vasthouden — alles hardop uitgesproken),
   minimaal 4 herhalingen, en langer als je hartslag nog niet ≤100 is.
4. **Onderdeel 2 — 3x 10 minuten rust** — geen muziek, jij start elke timer
   zelf. De timer blijft correct doorlopen als je naar een andere app gaat
   (bijv. om te gamen) en probeert een melding te sturen zodra de tijd om is —
   zet voor de zekerheid ook een losse telefoonwekker, want Android garandeert
   geen meldingen als de telefoon lang stil ligt in een andere app.
5. **Onderdeel 3 — 20 minuten afkoeling** — je 432Hz-playlist wordt geshuffled
   afgespeeld met een 20-minuten timer.

**Overslaan** — op elk scherm kun je delen overslaan: een losse piek, een
herstelfase, of een heel onderdeel (1, 2 of 3) in één keer.

## Stap 1 — Zet de app online (GitHub Pages, gratis)

1. Ga naar [github.com](https://github.com) en maak een gratis account (indien nog niet aanwezig).
2. Klik rechtsboven op **+** → **New repository**.
   - Naam: bijvoorbeeld `hiit-app`
   - Zet op **Public**
   - Klik **Create repository**
3. Klik op **Add file → Upload files** en sleep alle bestanden uit deze map
   erin: `index.html`, `manifest.json`, `sw.js`, `icon-192.png`, `icon-512.png`,
   `icon-512-maskable.png`.
4. Klik **Commit changes**.
5. Ga naar **Settings → Pages** (linkermenu).
   - Bij **Source** kies je **Deploy from a branch**
   - Branch: `main`, map: `/ (root)` → **Save**
6. Wacht ~1 minuut. Je vindt bovenaan de pagina je live link, iets als:
   `https://jouwgebruikersnaam.github.io/hiit-app/`

   **Bewaar deze exacte link** (inclusief de laatste `/`) — die heb je in
   stap 2 nodig.

## Stap 2 — Redirect URI instellen bij Spotify

1. Ga naar [developer.spotify.com/dashboard](https://developer.spotify.com/dashboard)
   en open je app (Client ID `b29daf7d8f5646f89c90a0241567a928`).
2. Klik **Settings**.
3. Bij **Redirect URIs** voeg je exact je GitHub Pages-link toe, bv.
   `https://jouwgebruikersnaam.github.io/hiit-app/`
4. Klik **Save**.

Dit moet exact overeenkomen (inclusief hoofdletters en de slash aan het einde),
anders werkt inloggen niet.

## Stap 3 — Tegel toevoegen op je Android-telefoon

1. Open de link uit stap 1 in **Chrome** op je telefoon.
2. Tik op het menu (⋮) rechtsboven → **App toevoegen** / **Toevoegen aan
   startscherm** (tekst kan iets verschillen per Chrome-versie).
3. Bevestig — er verschijnt nu een paarse tegel met hartslag-icoon op je
   beginscherm die de app opent als een echte app (geen adresbalk).

## Stap 4 — Eerste gebruik

1. Open de tegel.
2. Zet je hartslagband om en tik **Koppel hartslagband** — kies je band uit
   de lijst die verschijnt (Chrome vraagt mogelijk ook om locatietoegang;
   dat is een Android-vereiste voor Bluetooth-scannen, de app gebruikt je
   locatie verder nergens voor).
3. Open **Spotify** op je telefoon vast alvast (moet actief/open staan).
4. Tik **Verbind met Spotify** en log in / geef toestemming.
5. Zodra beide op groen staan wordt **Start training** klikbaar.

## Let op

- Bluetooth via de browser werkt alleen in **Chrome op Android** (niet in
  Firefox of andere browsers, en niet op iPhone — dat is een beperking van
  het besturingssysteem, niet van deze app).
- Spotify moet actief op je telefoon draaien tijdens de training (mag op de
  achtergrond); de app stuurt commando's naar de Spotify-app zelf, ze speelt
  niet in de browser.
- Onderaan elk trainingsscherm staat **Training stoppen** om terug te gaan
  naar het beginscherm, mocht dat nodig zijn.
