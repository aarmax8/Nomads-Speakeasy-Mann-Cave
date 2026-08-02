# Nomads Mann Cave

A mobile-first cocktail menu app with two rooms — The Cellar and The Mann Cave. It runs as a browser app and saves your favorites, bar stock, and any uploaded art on your device, so it works without accounts or a backend.

## What the app does

- Presents a card-based menu with double-sided drink cards
- Lets you flip between premium and well versions of the same drink
- Supports filtering by category, ingredient, glass type, favorites, and search
- Tracks what’s actually behind your bar so the deck can suggest drinks you can make
- Includes a favorites view, a stock view, a splash screen, a sound toggle, and a QR-based menu card
- Supports optional art for each drink, either from the repo or uploaded directly from your phone

## Put it online (GitHub Pages)

1. Create a new GitHub repository (public), for example `mann-cave`.
2. Upload these files to the repo root:
   - `index.html`
   - `manifest.json`
   - `apple-touch-icon.png`
   - `icon-512.png`
3. Open the repository’s Settings → Pages.
4. Set Source to Deploy from a branch, choose `main`, and use the `/root` folder.
5. Save the settings and wait a minute or two for the site to publish.

## Install it on your iPhone

1. Open the Pages URL in Safari.
2. Tap the Share button.
3. Choose Add to Home Screen.
4. Launch the app from the home-screen icon for the full-screen experience.

## Add art

If you want custom art, place image files in an `images/` folder in the repo and name them by drink slug. For example:

```text
images/old-fashioned.jpg
images/manhattan.jpg
images/whiskey-sour.jpg
images/margarita.jpg
images/daiquiri.jpg
images/mojito.jpg
images/moscow-mule.jpg
images/tom-collins.jpg
images/martini.jpg
images/sidecar.jpg
images/dark-n-stormy.jpg
images/paloma.jpg
```

The app will use those files automatically when present. You can also tap Add art on any card to upload an image from your phone; that version overrides the repo image and is stored locally on the device.

## Editing the menu

All drinks live in the `DRINKS` array near the top of the `<script>` in `index.html`. Ingredients for filtering and stock are defined in `INGREDIENTS` just above it.

To add a drink:
- Copy an existing drink object
- Update its fields
- Add its required ingredients to the `core` array using ids from `INGREDIENTS`

To add a new ingredient:
- Add it to `INGREDIENTS`
- Then reference its `id` in the relevant drinks

## Notes

- Everything runs in the browser.
- Favorites, bar stock, and local uploads are stored in browser storage on the device.
- Clearing browser data will reset those saved preferences.
