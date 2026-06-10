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

The QR codes (`qr.png`, `qr-card.png`) point to this URL.

## Files
- `index.html` — the menu (this is what the QR points to)
- `qr-card.png` — branded table card to print (cream QR tile, dark modules — scans reliably)
- `qr.png` — plain black-on-white QR code

## Editing the menu
Prices and items live in the `T` object inside `index.html` (one block per language).
Chicha prices are in `CHICHA`, flavors in `FLAVORS`. Edit, commit, push — the live site
updates automatically within ~1 minute.

## Regenerating the QR
If the live URL ever changes, regenerate both QR images so they keep pointing to the
right place. The card uses **dark modules on a cream tile** — never gold-on-black, which
is an inverted-luminance QR that many scanners refuse to read.

## Hosting (GitHub Pages)
Already enabled: `main` branch, `/root`. Push to `main` and the site redeploys.
