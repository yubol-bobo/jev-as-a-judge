# JEV-as-a-Judge — project website

Static HTML hosted at <https://yubol-bobo.github.io/jev-as-a-judge/>. No build step is required. GitHub Pages publishes the root of the `main` branch; `.nojekyll` disables Jekyll processing.

## Pages and manuscript

- `index.html`: interactive findings, charts, and arXiv BibTeX. All paper and repository links are ordinary HTML links that work without JavaScript. Chart data remain the September 2026 manuscript measurements.
- `paper.html`: the complete author-written abstract, title, authors, first-publication date, and Google Scholar citation metadata. It works without JavaScript or external fonts.
- `paper.pdf`: current author manuscript, synchronized from `paper/main_arxiv.pdf` in the research workspace on 24 September 2026. The author manuscript can contain revisions beyond the arXiv version; the separate arXiv link identifies the public version history.
- `sitemap.xml`: absolute URLs for the project homepage, abstract page, and PDF.

The paper is a preprint, first posted to arXiv on 22 September 2026: <https://arxiv.org/abs/2609.26550>. The site makes no journal or conference acceptance claim.

## Updating and deploying

Edit the HTML links directly; no JavaScript URL constants are used. When updating the manuscript, keep the hosted author PDF and the complete abstract in `paper.html` in sync. The four authors and full title should agree across the PDF, citation tags, and BibTeX. Keep `citation_pdf_url` absolute and in the same directory as the abstract page. `citation_publication_date` records the original public release, not each site edit.

Update sitemap `lastmod` only when the corresponding page or PDF materially changes. Commit the intended files and push `main` to deploy through the existing GitHub Pages configuration.

## Search indexing

1. Verify the URL-prefix property `https://yubol-bobo.github.io/jev-as-a-judge/` in Google Search Console, or use an already verified parent property. Use the actual HTML verification tag or file supplied by Google; keep it published after verification.
2. Submit <https://yubol-bobo.github.io/jev-as-a-judge/sitemap.xml> in Search Console.
3. Use URL Inspection for the homepage and `paper.html`, test each live URL, then request indexing.

The root site's `robots.txt` is maintained in the separate `yubol-bobo.github.io` repository. It already permits crawling. If desired, add this project's sitemap URL there as an additional `Sitemap:` line; a `robots.txt` inside this project directory would not control crawling.

Google Search requests do not guarantee inclusion or submit a paper to Google Scholar. Scholar discovers academic pages independently. Manually adding an article to an author profile is separate from indexing it in Scholar search.

Official references: [Google Scholar inclusion guidelines](https://scholar.google.com/intl/en/scholar/inclusion.html), [Search Console ownership verification](https://support.google.com/webmasters/answer/9008080), and [requesting Google recrawls](https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl).
