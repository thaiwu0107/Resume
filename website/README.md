# Thai Wu bilingual résumé website

Source for https://thai-wu-resume.ggttoo44.chatgpt.site

A buildless static website with Traditional Chinese and English pages, responsive dark styling, language navigation, print styles, and SEO metadata.

## Preview

From this directory:

    python3 -m http.server 8000 --directory dist

Visit http://localhost:8000/ (Chinese) or http://localhost:8000/en/ (English). Use a server rather than opening files directly because assets use root-relative URLs.

## Files

- `dist/index.html`: Chinese page, including crawlable résumé content.
- `dist/en/index.html`: English page, including crawlable résumé content.
- `dist/data.js`: matching bilingual content used by the page renderer.
- `dist/app.js`: navigation rendering and print behavior.
- `dist/style.css`: responsive and print styles.
- `dist/robots.txt`, `dist/sitemap.xml`: crawler metadata.

Update both static HTML and `data.js` when changing résumé content. If deploying to another origin, update canonical, alternate-language and social URLs, JSON-LD, robots.txt, and sitemap.xml. The files expect deployment at the origin root; a GitHub Pages project subpath needs path adjustments.

This source export does not change the existing hosted website or configure GitHub Pages. Hosting credentials and provider-specific configuration are excluded.
