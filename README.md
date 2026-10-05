# Welcome to Coolsville — Lookbook

An online lookbook for *Welcome to Coolsville*, a Rickie Lee Jones documentary
directed by Michael Gramaglia. Ten slides, navigated with the arrow keys.

## Viewing it

Open `index.html` in a browser. No build step, no dependencies, no server
required — though if your browser blocks local font loading, run a tiny server
from this folder instead:

```
python3 -m http.server 8000
```

…then visit <http://localhost:8000>.

## Publishing on GitHub Pages

1. Push this folder to a repository.
2. **Settings → Pages → Build and deployment → Deploy from a branch.**
3. Pick your branch and the `/ (root)` folder, then save.

The `.nojekyll` file is already included so Pages serves the directory as-is.

## Navigation

| Input | Action |
| --- | --- |
| `→` `↓` `Space` `PageDown` | Next slide |
| `←` `↑` `PageUp` | Previous slide |
| `Home` / `End` | First / last slide |
| Click left or right page edge | Previous / next |
| Swipe | Previous / next (touch devices) |

The URL hash tracks the current slide, so `index.html#7` deep-links to slide 7
and the browser back button steps through your history.

## Structure

```
index.html              markup, styles and navigation — everything in one file
assets/img/             slide photography (JPEG)
assets/fonts/           Cossette Titre & Cossette Texte (WOFF2)
```

The layout scales from a fixed 16:10 stage using CSS container query units
(`cqw`), so every type size and margin stays in proportion at any window size.
To restyle, the design tokens sit at the top of the `<style>` block in
`index.html`.

## Typefaces

Cossette Titre (headlines) and Cossette Texte (body), both by Coppers and Brasses,
used under the SIL Open Font License 1.1. See
<https://fonts.google.com/?query=cossette>.

## Image rights

The photography in this lookbook is **not cleared for public distribution**.
The archival and press images have photographers attached — including an Annie
Leibovitz portrait — and the "Welcome to Coolsville" billboard frame is an
AI-generated concept image, not a photograph. Clear all of it before this goes
anywhere public, and consider keeping the repository private in the meantime.
