# Korantemaa Agyekum — Portfolio

Multi-page bilingual portfolio (EN source, FR toggle), same design system as Roland Dzoagbe's site.
Pages: index, about, experience, impact, expertise, leadership, contact, 404.

## Publish (GitHub Pages)
1. In the `o-agyekum/Korantemaa` repository, delete the old site files and copy every file from this folder to the repository root (keep `.nojekyll`).
2. Settings → Pages → Source: "Deploy from a branch", branch `main`, folder `/ (root)`.
3. The site is served at https://o-agyekum.github.io/Korantemaa/

## Before publishing: replace every [bracketed] placeholder
Search all files for `[` to find them. They are:
- **Full name**: currently "Korantemaa Agyekum" (brand, titles, footer, favicon initials "KA"). If the surname is different, search-and-replace it in every .html file and in app.js.
- **Contact**: `[email@example.com]`, `[+33 6 …]`, `[linkedin.com/in/…]` in index.html, contact.html and the footer of every page.
- **Experience dates and titles** (experience.html + French copies in app.js): Danone start year, Eutelsat end year and job title, the bank's name and city (2013–2018).
- **Education and certifications** (experience.html): two education lines, certification line, other treasury systems.
- **Tools** (expertise.html): `[TMS / ERP]`, `[Banking platforms]`.
- **Recommendations** (leadership.html): paste LinkedIn recommendations or delete the two placeholder cards.
- **Photo**: add `profile.jpg` (square, at least 600×600). Without it the site shows the initials.
- **CVs**: add `Korantemaa_Agyekum_CV_EN.pdf` and `Korantemaa_Agyekum_CV_FR.pdf` at the root, or remove the CV links (footer + contact page).

## How translations work
English text lives in the HTML. French lives in `app.js` under `T.fr`, keyed by `data-i18n`. When you change an English sentence in the HTML, update the matching French value in app.js.

## Cache and updates
Every deploy should change the `build` id in all pages, `version.json`, and the `?v=` on styles.css / app.js (they are the same value). Open tabs auto-refresh when version.json changes.
