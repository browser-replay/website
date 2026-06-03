# browserreplay-website

Source for [browserreplay.com](https://browserreplay.com) — the landing page for the [browser-replay](https://github.com/browser-replay/browser-replay) open source project.

## Structure

```
.
├── index.html          # Main landing page
├── styles/
│   └── main.css        # All styles
├── public/
│   ├── favicon.ico     # Add your favicon here
│   └── og-image.png    # Add your Open Graph image here (1200×630px recommended)
└── .github/
    └── workflows/
        └── deploy.yml  # Auto-deploys to GitHub Pages on push to main
```

## Local development

No build step required. Open `index.html` directly in a browser, or use any static file server:

```bash
npx serve .
```

## Deployment

The site deploys automatically to GitHub Pages on every push to `main` via the included workflow.

To enable GitHub Pages on a new repo:
1. Go to **Settings → Pages**
2. Set **Source** to **GitHub Actions**

To use a custom domain, add a `CNAME` file to this repo containing your domain:

```
browserreplay.com
```

Then configure your DNS to point at GitHub Pages ([docs](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site)).
