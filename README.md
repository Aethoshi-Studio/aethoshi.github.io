# Aethoshi website

The Aethoshi studio site, served by GitHub Pages at
<https://aethoshi-studio.github.io/>. Plain HTML, one stylesheet and an SVG
logo, with no build step and no scripts.

| Path | What |
|---|---|
| `/` (`index.html`) | Home: our apps, About Aethoshi (the name, what we believe) at `/#about`, contact |
| `/parchi/` | About the Parchi billing app: features, data, ads, help |
| `/parchi/privacy/` | Parchi privacy policy (the URL given to Google Play) |
| `/app-ads.txt` | AdMob seller line. It must be at the **domain root** |
| `404.html` | Page shown for unknown URLs |
| `assets/logo.svg` | The Aethoshi logo (sunrise over the horizon); also the favicon |
| `assets/parchi-icon.png` | Parchi's app icon (from the app's `assets/icon/play_store_512.png`) |
| `assets/style.css` | All styles: colour tokens, light and dark mode, phone layout |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

All links are **relative** (`assets/…`, `../assets/…`), so the pages work
at the domain root, in a sub-folder, or opened straight from disk.

## Publishing

1. The repository must be named **`aethoshi-studio.github.io`** under the
   `aethoshi-studio` account. Only that name is served at the domain
   root. Any other name, like `aethoshi.github.io`, ends up at
   `https://aethoshi-studio.github.io/aethoshi.github.io/`, where AdMob
   can't find `app-ads.txt`. To rename it: Settings → General → Repository
   name.
2. Push to `main`, then Settings → Pages → *Deploy from a branch*,
   `main`, `/ (root)`.
3. After a minute or two, check:
   - <https://aethoshi-studio.github.io/>
   - <https://aethoshi-studio.github.io/parchi/privacy/>
   - <https://aethoshi-studio.github.io/app-ads.txt>

## Updating

- **Privacy policy:** edit `parchi/privacy/index.html` and change the
  "Effective" date at the top.
- **app-ads.txt:** the line must match the one AdMob shows under
  Apps → Parchi → app-ads.txt.
- **Launch:** when Parchi is on Google Play, replace "Coming soon to Google
  Play" on the home and Parchi pages with a link to the store listing.
- **Preview locally:** open `index.html` in a browser, or run
  `python3 -m http.server` in this folder and visit <http://localhost:8000>.
