# Aethoshi website

The Aethoshi studio site, served by GitHub Pages at
**<https://aethoshi-studio.github.io/aethoshi.github.io/>** (this
repository, `aethoshi.github.io`, on the `aethoshi-studio` account).
Plain HTML, one stylesheet and the brand logo, with no build step and no
scripts.

| Path | What |
|---|---|
| `/` (`index.html`) | Home: our apps, About Aethoshi (the name, what we believe) at `#about`, contact |
| `/parchi/` | About the Parchi billing app: features, data, ads, help |
| `/parchi/privacy/` | Parchi privacy policy (the URL given to Google Play) |
| `404.html` | Page shown for unknown URLs |
| `assets/aethoshi-logo.png` | Full logo (star, orbit, AETHOSHI STUDIO), cut from `aethoshi logos/Aethoshi Cosmic Studio Logo.png` |
| `assets/aethoshi-symbol.png` | The star-and-orbit symbol alone (header, footer, About) |
| `assets/favicon.png` | Tab icon (the symbol, 64 px) |
| `assets/parchi-icon.png` | Parchi's app icon |
| `assets/style.css` | All styles: colour tokens, light and dark mode, phone layout |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

**The logo is black on white.** Anything with `class="mark"` is blended
into the page. In light mode it multiplies (white disappears); in dark mode
it's inverted and screened (black disappears). So the one PNG works on both
themes. If you replace it, keep it black on a white background.

All links are **relative** (`assets/…`, `../assets/…`), so the pages work
at any address and when opened straight from disk.

## app-ads.txt is not here

AdMob reads `app-ads.txt` only from the **domain root**,
`https://aethoshi-studio.github.io/app-ads.txt`. This site lives in a
sub-folder, so the file is in a separate repository,
`aethoshi-studio.github.io`, which also forwards the root address to this
site. See that repository's README.

## Publishing

Push to `main`. Settings → Pages: *Deploy from a branch*, `main`,
`/ (root)`. Check:

- <https://aethoshi-studio.github.io/aethoshi.github.io/>
- <https://aethoshi-studio.github.io/aethoshi.github.io/parchi/privacy/>

## Updating

- **Privacy policy:** edit `parchi/privacy/index.html` and change the
  "Effective" date at the top.
- **Launch:** when Parchi is on Google Play, replace "Coming soon to Google
  Play" on the home and Parchi pages with a link to the store listing.
- **Preview locally:** open `index.html` in a browser, or run
  `python3 -m http.server` in this folder and visit <http://localhost:8000>.
