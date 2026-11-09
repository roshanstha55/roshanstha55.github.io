# Vexel Interactive website

Static site served by GitHub Pages at https://roshanstha55.github.io/.

## Layout

| Path | What |
|---|---|
| `index.html`, `style.css` | Studio home: one card per app |
| `404.html` | Not-found page for the whole site |
| `sitemap.xml`, `robots.txt` | For search engines |
| `<app>/` | Everything for one app: `index.html` (app page), `privacy.html`, `terms.html`, `style.css`, icon, screenshots and any extra pages |
| `glowmere/` | Glowmere: Logic Puzzles (app page, privacy, terms, FAQ, how to solve, challenge links in `c/`) |
| `nfckit/` | NFC Kit: Tag Reader & Writer (app page, privacy, terms, screenshots) |
| `app-ads.txt`, `.well-known/`, `.nojekyll`, `google1771b16c69684ef6.html` | Required at the root by AdMob, Android app links, GitHub Pages and Google verification. Don't move them |

App URLs never change once they're in a Play listing (privacy and terms especially), so an app keeps its folder name for good.

## Adding an app

1. Make a folder named after the app (lowercase, no spaces), e.g. `myapp/`.
2. Add `myapp/index.html`, `myapp/privacy.html`, `myapp/terms.html`, `myapp/style.css` and an icon. Copy the structure of `nfckit/`: a breadcrumb `Vexel Interactive › App` linking to `../`, and a footer linking to `../`, privacy, terms and the support email.
3. Add a card for it in the root `index.html` (copy an existing `<li class="card app">`).
4. Add its pages to `sitemap.xml`, and a line to `404.html`.
5. Use the app's own URLs in its Play listing: `https://roshanstha55.github.io/myapp/`, `.../myapp/privacy.html`.

## Rules

Fully static. No redirects of any kind, no `intent://` links, never render text taken from URL parameters, no imitation Play badges (a plain text link is fine once the app is live), no forms, no external scripts or fonts, no hidden content.
