# JEV as a Judge — project page

Single static page (`index.html`), no build step, no dependencies beyond Google Fonts. All numbers are typed into the `DATA` block at the bottom of `index.html` and come from the manuscript of 2026-09-21.

## Deploy on GitHub Pages (user `yubol-bobo`, repo `jev-as-a-judge`)

```bash
git init jev-as-a-judge && cd jev-as-a-judge
cp -r /path/to/site/* .          # index.html, README.md, .nojekyll
git add . && git commit -m "Project page"
git branch -M main
git remote add origin git@github.com:yubol-bobo/jev-as-a-judge.git
git push -u origin main
```

Then on GitHub: **Settings → Pages → Build and deployment → Source: Deploy from a branch → Branch: `main` / `(root)` → Save.**
The page appears at <https://yubol-bobo.github.io/jev-as-a-judge/> within a minute or two. `.nojekyll` keeps GitHub from running Jekyll over the folder.

If the repository also holds code, put the page in a `docs/` folder and choose `main` / `/docs` instead.

## Two lines to edit before publishing

At the very end of `index.html`:

```js
const PAPER_URL='#paper-link';   // e.g. 'paper.pdf' (drop the PDF next to index.html) or an arXiv URL
const CODE_URL='#code-link';     // e.g. 'https://github.com/yubol-bobo/jev-as-a-judge'
```

Every Paper / Code button on the page reads these two constants. The BibTeX block near the end of the file is a placeholder until the paper has a venue.

## Notes

- The manuscript is under anonymous review at ACL Rolling Review. Current ACL policy has no anonymity period, so a public page is allowed, but do not advertise the submission to reviewers (no posts aimed at the reviewing community) while it is under review. The page says "under review" and makes no acceptance claim.
- Prices, latencies, and model identifiers reflect September 2026; the footer says so.
- Motion respects `prefers-reduced-motion`. Every chart has a hover tooltip; the accuracy chart has a "View data" table.
