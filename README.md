# Cakeology Mombasa

A front-end for Cakeology — a modern, responsive UI built with HTML, SCSS and JavaScript. This repository primarily contains the static front-end assets for the Cakeology microservices/application. Use this README as a starting point and adapt any commands or paths to match your project's actual build system.

- Primary languages:
  - HTML — 49.4%
  - SCSS — 32.6%
  - JavaScript — 15.6%
  - CSS — 2.4%

## Table of contents
- [About](#about)
- [Live demo / Screenshots](#live-demo--screenshots)
- [Features](#features)
- [Tech stack](#tech-stack)
- [Project structure (suggested)](#project-structure-suggested)
- [Getting started (local development)](#getting-started-local-development)
- [Build & deploy](#build--deploy)
- [Hosting & cost considerations](#hosting--cost-considerations)
- [What I learned](#what-i-learned)
- [Contributing](#contributing)
- [Troubleshooting](#troubleshooting)
- [Todo / Improvements](#todo--improvements)
- [License](#license)
- [Contact](#contact)

## About
Cakeology MSA contains the frontend UI components and static pages for the Cakeology application. It focuses on markup (HTML), styles (SCSS/CSS) and client-side JavaScript. The repo is organized for easy development, theming, and static deployment.

> Note: If this repository is part of a larger microservices system, use this repo as the front-end artifact that consumes APIs provided by backend services.

## Live demo / Screenshots
Live demo: https://cakeologyke.com

Add screenshots or local preview images to `docs/screenshots/`, for example:
- `docs/screenshots/homepage.png`
- `docs/screenshots/product-page.png`

## Features
- Responsive layout built with semantic HTML
- Styles written in SCSS for modular, maintainable styling
- Lightweight JavaScript for interactivity (forms, modals, client-side validation)
- Easy to build and deploy as a static site

## Tech stack
- HTML5
- SCSS / Sass
- JavaScript (vanilla or framework-agnostic)
- Optional build tools: Node.js, npm/yarn, PostCSS, Autoprefixer, Sass compiler

## Project structure (suggested)
If your repo is arranged differently update these paths below to match your codebase.

- index.html
- src/
  - assets/         — images, fonts
  - js/             — JavaScript source files
  - scss/           — SCSS source files (partials, components)
- dist/ or public/  — compiled output for deployment
- docs/             — screenshots, design notes

## Getting started (local development)

1. Install Node.js (v16+ recommended) and npm or yarn.

2. Install dependencies (if a package.json is present):
```bash
npm install
# or
yarn install
```

3. Development (example scripts — adjust to your repo):
```bash
# If using a dev server (e.g., live-server, serve, or a bundler)
npm run dev

# To compile SCSS -> CSS (example using dart-sass)
npx sass src/scss:dist/css --watch

# Or a combined script
npm run start
```

If your repo does not use npm scripts, you can compile SCSS manually:
```bash
npx sass src/scss/main.scss:dist/css/main.css --style=expanded
```

Open `index.html` in your browser or use a static server:
```bash
npx serve dist
```

## Build & deploy
Create a production build (example):
```bash
npm run build
# Example build steps might include:
# - compile SCSS
# - minify CSS/JS
# - copy assets to dist/
```

Deploy `dist/` or `public/` to any static host:
- GitHub Pages
- Netlify
- Vercel
- Firebase Hosting
- AWS S3 + CloudFront
- Any cPanel-based shared hosting (less recommended for scale/cost)

## Hosting & cost considerations
When choosing where to host the front-end, consider:

- Traffic pattern and bandwidth costs — static hosting (Netlify, Vercel, GitHub Pages) is often cheapest for low-to-moderate traffic.
- Storage and build minutes — some providers charge for build time or larger storage needs.
- DNS and domain management — some registrars include DNS; external DNS providers may charge separately.
- Ease of migration — static sites are straightforward to migrate from cPanel-based shared hosting to cloud providers like AWS S3 + CloudFront for cost efficiency at scale.
- Security & SSL — ensure automatic TLS (many static hosts provide this for free).

Common DNS setup notes:
- For S3 + CloudFront, point your domain's A/ALIAS record to the CloudFront distribution.
- For Netlify/Vercel, create the provider-specified CNAME or A records.
- For cPanel/shared hosting, update the domain's nameservers or A record to the hosting provider.

## What I learned
During development and deployment of this project I learned a lot about hosting, DNS management, and cost optimisation:

- I explored cPanel-based shared hosting and how traditional hosting providers bill for domains, DNS and resource use.
- I evaluated cloud alternatives and rolled services over to AWS for greater cost-effectiveness and scalability.
- I learned to compare provider pricing (bandwidth, storage, DNS, build minutes) to determine the most cost-effective setup for a static front-end.
- Practical skills gained: using cPanel, migrating static assets, configuring DNS records, and setting up AWS S3 + CloudFront for static hosting.

Include specifics about the migration steps, DNS records you used, or configuration snippets here to document the exact process for future maintainers.

## Contributing
Thank you for your interest in improving Cakeology!

- Fork the repo
- Create a feature branch: `git checkout -b feat/your-feature`
- Make changes and commit with clear messages
- Open a pull request describing your changes

Add/update documentation, screenshots, and tests where applicable.

## Troubleshooting
- SCSS compilation errors: check import paths and variable definitions
- Styling not updating: ensure compiled CSS is the one being served (clear cache)
- JavaScript errors: check browser console and confirm script order in HTML
- DNS issues: verify propagation with `dig`/`nslookup` and check TTLs

If you run into a blocking issue, create an issue with reproduction steps and expected vs actual behavior.

## Todo / Improvements
- Add a full contributing guide (CONTRIBUTING.md)
- Add CI/CD pipeline for build and deploy
- Provide design system and component documentation (Storybook or docs site)
- Add unit/integration tests for JavaScript behavior
- Document the exact migration steps and cost comparison that were used when moving off cPanel to AWS
- Add screenshots and link them from this README

## License
Specify a license for the project, for example:
MIT © Your Name

(Replace with the correct license and author information.)

## Contact
Maintainer: NaeemChakera
Website / demo: https://cakeologyke.com

If you want, I can:
- open a PR adding this README to the `main` branch,
- tailor the content to exact scripts/paths found in your repo, or
- add badges (CI, license, etc.) if you point me to your CI or license files.
