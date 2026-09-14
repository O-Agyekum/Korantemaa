# Korantemaa Ofei-Agyekum — Portfolio

Multi-page bilingual portfolio (EN source, FR toggle), same design system as Roland Dzoagbe's site.
Pages: index, about, experience, impact, expertise, leadership, contact, 404.

## Publish (GitHub Pages)
1. In the `o-agyekum/Korantemaa` repository, delete the old site files and copy every file from this folder to the repository root (keep `.nojekyll`).
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site is served at https://o-agyekum.github.io/Korantemaa/

## Remaining items to confirm
Contact details, dates, titles, education and tools were filled from the two CV PDFs in the repository.
- **Photo**: add `profile.jpg` (square, at least 600×600). Without it the site shows the initials.
- **Story vs CV**: the original narrative mentioned five years in banking (2013–2018) and Eutelsat from 2018; the site follows the CV (Ecobank 2018–2020, Eutelsat 2021–2022, Danone since 2022). Adjust if the CV is incomplete.

## How translations work
English text lives in the HTML. French lives in `app.js` under `T.fr`, keyed by `data-i18n`. When you change an English sentence in the HTML, update the matching French value in app.js.

## Cache and updates
Every deploy should change the `build` id in all pages, `version.json`, and the `?v=` on styles.css / app.js (they are the same value). Open tabs auto-refresh when version.json changes.
