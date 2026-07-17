# Nomads Mann Cave

A single-file cocktail app. Two rooms — **The Cellar** (speakeasy, top-shelf pours) and **The Mann Cave** (dive bar, well spirits). Every card is double-sided, so one flip swaps the same drink between premium and well versions. Filter by ingredient, mark what's behind your bar, and the deck only stops on drinks you can actually make.

Everything runs in the browser. Your bar stock and any art you upload are saved on your phone — no accounts, no server.

## Put it online (GitHub Pages)

1. Create a new GitHub repository (public), e.g. `mann-cave`.
2. Upload these files to the repo root:
   - `index.html`
   - `manifest.json`
   - `apple-touch-icon.png`
   - `icon-512.png`
3. Repo **Settings → Pages** → Source: **Deploy from a branch** → branch `main`, folder `/root` → **Save**.
4. Wait ~1 minute. Your app is live at `https://YOURNAME.github.io/mann-cave/`.

## Add your David Mann art

The Mann Cave side of each card looks for an image in an `images/` folder, by drink name. Create a folder called `images` in the repo and drop your scans in, named exactly like this (`.jpg`, `.jpeg`, `.png`, or `.webp` all work):

```
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

Each frame fills automatically once its file is in the repo. You can also tap **Add art** on any card to load an image straight from your phone — that one is saved on-device and overrides the repo file. Tap **Replace** or the trash icon to change it.

## Install it on your iPhone (runs like an app)

1. Open the Pages URL in **Safari**.
2. Tap the **Share** button → **Add to Home Screen** → **Add**.
3. Launch it from the home-screen icon — it opens full-screen with no browser bars.

## Editing the menu

All drinks live in the `DRINKS` array near the top of the `<script>` in `index.html`. Ingredients for filtering and stock live in `INGREDIENTS` right above it. To add a drink, copy one entry, change the fields, and list its core ingredients in `core` (using ids from `INGREDIENTS`). To add a brand-new ingredient, add it to `INGREDIENTS` first, then reference its `id`.
