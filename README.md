# Welcome to Coolsville — Lookbook

The film pitch deck for *Welcome to Coolsville*, a Rickie Lee Jones documentary
directed by Michael Gramaglia. Eleven slides, navigated with the arrow keys.

Three of the slides pair a **cinematic reference** still against **the vision**
frame it informs — Wizard of Oz against the cornfield, One from the Heart
against the floating Vega, and so on.

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

The imagery here is **not cleared for public distribution** and falls into three
distinct categories, which matter for different reasons:

- **Archival and press photographs of Rickie Lee Jones** — these have
  photographers attached, including an Annie Leibovitz portrait. They need
  licensing.
- **Film stills** used as cinematic reference (The Wizard of Oz, 8½, One from
  the Heart, Wings of Desire, Rocketman). Studio-owned; fine for an internal
  pitch, not for publication.
- **Generated concept frames** in the "vision" column. These are
  AI-generated illustrations of scripted scenes, not photographs of anyone, and
  are deliberately composed so no figure is identifiable. Label them as concept
  art wherever this deck travels.

Keep this repository private until the first two categories are cleared.
