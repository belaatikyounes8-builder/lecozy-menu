# Le Cozy — Digital QR Menu

Multilingual, time-aware digital menu for Le Cozy lounge & chicha bar.

## Features
- Time-aware greeting (morning/afternoon/evening/night) with live clock
- 5 languages: English, Français, العربية, Español, Русский
- Automatic RTL layout for Arabic
- Mobile-first, collapsible sections
- Black & gold premium design

## Live menu
**https://belaatikyounes8-builder.github.io/lecozy-menu/**

All QR codes point to this URL.

## Files
- `index.html` — the menu (this is what the QR points to)
- `qr-card.png` — branded table card to print (cream QR tile + gold hookah medallion in the center)
- `qr.png` — standalone QR with the hookah medallion (cream background)
- `qr-plain.png` — plain black-on-white QR, no logo (fallback for tiny prints / low-quality surfaces)
- `hookah.png`, `logo.png` — brand assets used in the card

## Editing the menu
Prices and items live in the `T` object inside `index.html` (one block per language).
Chicha prices are in `CHICHA`, flavors in `FLAVORS`. Edit, commit, push — the live site
updates automatically within ~1 minute.

## Regenerating the QR
If the live URL ever changes, regenerate the QR images so they keep pointing to the
right place. Two rules learned the hard way:
- Use **dark modules on a cream/light tile** — never gold-on-black, which is an
  inverted-luminance QR that many scanners refuse to read.
- The center hookah medallion relies on **error-correction level H** (~30% redundancy)
  and a cream gutter behind it. Keep the logo ≲ 25% of the QR width and re-verify the
  code still decodes (e.g. with `zbar`/`pyzbar`) before printing.

## Hosting (GitHub Pages)
Already enabled: `main` branch, `/root`. Push to `main` and the site redeploys.
