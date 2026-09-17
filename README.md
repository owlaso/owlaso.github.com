# OwlASO — Landing Page

Marketing site for **OwlASO**, the open-source ASO keyword tracking & app store review analytics desktop app.

- **App repo:** <https://github.com/owlaso/owlaso>
- **Live site:** deployed to GitHub Pages via the included workflow

## Stack

- [Vite](https://vitejs.dev) + vanilla JS/CSS, single page
- Dark/light theme with manual toggle and OS-preference detection
- Theme-aware product screenshots (`aso.png` / `aso-light.png`, `reviews.png` / `reviews-light.png`) that switch with the theme

## Develop

```bash
npm install
npm run dev      # local dev server on :3000
npm run build    # production build -> dist/
npm run preview  # preview the production build
```

## Deploy

Push to `main`. The GitHub Actions workflow (`.github/workflows/deploy.yml`) builds the site and publishes it to GitHub Pages. `dist/` and `node_modules/` are gitignored — the build step produces the deployable artifact.

## Optional: Vercel

`vercel.json` pins the build/output for Vercel and adds security headers (`X-Frame-Options`, `X-Content-Type-Options`, `Referrer-Policy`, `Permissions-Policy`) if you prefer to serve it there instead.