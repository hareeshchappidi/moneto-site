# Moneto — website

The public site for **Moneto**, a private, offline expense tracker for iPhone (“Know where your money goes.”).
Plain HTML and CSS — no build step, no frameworks, no cookies, no analytics, no third-party requests.

| Page | Path | Used for |
|---|---|---|
| Home | `index.html` | Landing page with screenshots and features |
| Privacy policy | `privacy.html` | App Store Connect **Privacy Policy URL**; in-app link |
| Support | `support.html` | App Store Connect **Support URL**; FAQ and contact |
| Terms of use | `terms.html` | Optional; points to Apple’s standard EULA |
| Not found | `404.html` | GitHub Pages error page |

## Deploy with GitHub Pages

1. Repository **Settings → Pages**.
2. **Source:** Deploy from a branch · **Branch:** `main` · **Folder:** `/ (root)` → Save.
3. After a minute the site is live at **https://laavi.in/**.

URLs for App Store Connect:

- Privacy Policy URL: `https://laavi.in/privacy.html`
- Support URL: `https://laavi.in/support.html`
- Marketing URL (optional): `https://laavi.in/`

### Custom domain (optional)

Add a `CNAME` file containing the domain (e.g. `moneto.app`), point the domain’s DNS at GitHub Pages, and update the
absolute URLs in `robots.txt`, `sitemap.xml` and the `/moneto-site/` paths in `404.html`.

## Updating

- **Screenshots** (`assets/screens/*.jpg`, 600 × 1300) are taken from the iOS Simulator with the sample data in US dollars,
  with neutral account names (no real bank names): Home, Insights, Cash flow, Accounts, Activity and a PDF report.
- **Icon** (`assets/icon-512.png`, `apple-touch-icon.png`, `favicon-64.png`) comes from the app’s
  `AppIcon-1024.png`.
- Keep `privacy.html` in step with the app’s in-app privacy policy, and change the **Effective** date whenever it changes.
- Colours in `assets/styles.css` mirror the app’s design tokens, with light and dark mode.

## Local preview

```bash
python3 -m http.server 8000
```

Then open http://localhost:8000.
