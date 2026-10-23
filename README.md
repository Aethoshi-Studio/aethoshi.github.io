# aethoshi.github.io

The Aethoshi website, served by GitHub Pages at <https://aethoshi.github.io>.
Plain HTML and one stylesheet, with no build step.

| Path | What |
|---|---|
| `/` (`index.html`) | Home: our apps, and About Aethoshi (the name, what we believe) at `/#about` |
| `/parchi/` | About the Parchi billing app |
| `/parchi/privacy/` | Parchi privacy policy (the URL given to Google Play) |
| `/app-ads.txt` | AdMob seller line. It must stay at the site root |
| `404.html` | Page shown for unknown URLs |
| `.nojekyll` | Tells GitHub Pages to serve the files as they are |

## Publishing

1. Create a **public** GitHub repository named exactly `aethoshi.github.io`
   under the `aethoshi` account.
2. Push these files to its `main` branch.
3. Go to Settings → Pages → Build and deployment → Source:
   *Deploy from a branch*, Branch: `main`, folder `/ (root)`. Save.
4. After a minute or two, check:
   - <https://aethoshi.github.io/>
   - <https://aethoshi.github.io/parchi/privacy/>
   - <https://aethoshi.github.io/app-ads.txt>

## Updating

- **Privacy policy:** edit `parchi/privacy/index.html` and change the
  "Effective" date at the top.
- **app-ads.txt:** the line must match the one AdMob shows under
  Apps → Parchi → app-ads.txt.
- **Launch:** when Parchi is on Google Play, replace "Coming soon to Google
  Play" on both pages with a link to the store listing.
