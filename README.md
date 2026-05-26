# gabriel.js.org

Animated static portfolio for **Gabriel Clemente** — full-stack JavaScript/TypeScript engineer in Zürich. Built for [GitHub Pages](https://pages.github.com/) with a custom [js.org](https://js.org) subdomain.

**Live URL (after setup):** https://gabriel.js.org

## Features

- Static-first HTML, CSS, and minimal JavaScript (no framework on the page)
- Animated intro sequence, scroll reveals, ambient gradient background, and particle canvas
- Dark/light theme toggle with system preference support
- i18n: English, Spanish, German (browser language detection)
- SEO: JSON-LD (`Person`, `WebSite`, `FAQPage`), Open Graph, sitemap, `llms.txt`

## Deploy to GitHub Pages

1. Push this repo to `Gabo-Tech/gabriel` on GitHub.
2. In the repository, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source** to **Deploy from a branch**.
4. Choose branch **`main`**, folder **`/ (root)`**, and save.
5. Under **Custom domain**, enter `gabriel.js.org` and save. GitHub will create/update the `CNAME` file (this repo already includes `CNAME` with that value).
6. Enable **Enforce HTTPS** once DNS is verified.

The site will be available at `https://gabo-tech.github.io/gabriel/` until the custom domain propagates.

## Request the js.org subdomain

After GitHub Pages is live with real content:

1. Fork [js-org/js.org](https://github.com/js-org/js.org).
2. Edit `cnames_active.js` and add (in alphabetical order):

   ```js
   "gabriel": "gabo-tech.github.io/gabriel",
   ```

3. Open a pull request using [their template](https://github.com/js-org/js.org/blob/master/PULL_REQUEST_TEMPLATE.md).
4. In the PR description, link to https://gabo-tech.github.io/gabriel/ (or https://gabriel.js.org once DNS works) and explain that the site is a JavaScript engineer portfolio with case studies, OSS links, and production stack details.

js.org typically activates the subdomain within 24 hours after merge.

## Local preview

Any static file server works:

```bash
python3 -m http.server 8080
```

Then open http://localhost:8080 (from the repo root).

## Structure

| File | Purpose |
|------|---------|
| `index.html` | Main portfolio page |
| `styles.css` | Layout, theme, animations |
| `portfolio.js` | i18n, theme, intro, scroll effects, work list |
| `portfolioItems.json` | Selected work / case studies data |
| `CNAME` | Custom domain for GitHub Pages |
| `Gabriel Clemente Resume.pdf` | Downloadable résumé |

## License

Portfolio content © Gabriel Clemente. Site code in this repository is provided for hosting this personal portfolio.
