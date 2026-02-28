<p align="center">
  <img src="public/logo.svg" alt="Meappy" width="80" height="80" />
</p>

<h1 align="center">meappy.com</h1>

<p align="center">
  <strong>Technology Solutions & Automation</strong>
</p>

<p align="center">
  <a href="https://github.com/meappy/meappy.com/actions/workflows/deploy.yml"><img src="https://github.com/meappy/meappy.com/actions/workflows/deploy.yml/badge.svg" alt="Deploy" /></a>
  <a href="https://meappy.com"><img src="https://img.shields.io/website?url=https%3A%2F%2Fmeappy.com&label=meappy.com" alt="Website" /></a>
  <img src="https://img.shields.io/github/languages/top/meappy/meappy.com" alt="Language" />
  <img src="https://img.shields.io/github/license/meappy/meappy.com" alt="Licence" />
</p>

---

Business portfolio website for **Meappy**, a technology consultancy specialising in Infrastructure & DevOps, AI Automation, E-commerce Integration, and Custom Web & Mobile solutions.

## Stack

- **Framework** — [Astro](https://astro.build/) (static output)
- **Styling** — Scoped CSS, no external dependencies
- **Hosting** — GitHub Pages
- **DNS/CDN** — Cloudflare
- **CI/CD** — GitHub Actions (`withastro/action`)

## Project Structure

```
src/
├── components/
│   ├── Header.astro      # Sticky nav with inline SVG logo
│   ├── Hero.astro         # Hero section with gradient title
│   ├── Services.astro     # 4 service cards
│   ├── About.astro        # Company bio + highlights
│   ├── Contact.astro      # Email contact card
│   └── Footer.astro       # Footer with links
├── layouts/
│   └── Layout.astro       # Base HTML shell (SEO, OG, fonts)
└── pages/
    └── index.astro        # Single page assembling all components
```

## Local Development

### With Docker

```bash
docker compose up --build
```

Site available at `http://localhost:4321`.

### Without Docker

```bash
npm install
npm run dev
```

## Deployment

Pushes to `main` trigger a GitHub Actions workflow that builds the site and deploys to GitHub Pages. Cloudflare DNS proxies `meappy.com` to `meappy.github.io`.

## Commands

| Command             | Action                                    |
| :------------------ | :---------------------------------------- |
| `npm run dev`       | Start local dev server at `localhost:4321` |
| `npm run build`     | Build production site to `./dist/`         |
| `npm run preview`   | Preview build locally before deploying     |
