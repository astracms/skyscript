# SkyScript

[![Built with Astro](https://astro.badg.es/v2/built-with-astro/tiny.svg)](https://astro.build/themes/details/skyscript)
[![CI](https://github.com/astracms/skyscript/actions/workflows/ci.yml/badge.svg)](https://github.com/astracms/skyscript/actions/workflows/ci.yml)

**SkyScript** is a modern, content-first blog starter built with **Astro v5**, **Tailwind CSS v4**, and **AstraCMS**. Designed for SEO optimization and responsiveness across all devices, it's perfect for personal blogs, company blogs, and content-focused websites.

## Features

- [x] Modern & minimalist design with responsive layout
- [x] AstraCMS integration for headless content management
- [x] Static site generation for optimal performance
- [x] SEO optimization (Open Graph, Twitter Cards, Canonical URLs)
- [x] Centralized site configuration via `constants.ts`
- [x] Dynamic meta tags from post content
- [x] Featured posts and category-based organization
- [x] Pagination support
- [x] Author cards and related posts
- [x] Newsletter subscription component
- [x] TypeScript support
- [x] Component-based architecture
- [x] Tailwind CSS v4 for styling
- [x] Code quality tools (ESLint & Prettier)
- [x] View Transitions API support
- [x] Automatic sitemap generation

![LightRoom Test](/assets/pagespeed-insights.png)

## Project Structure

```
SkyScript
├── public/
│   ├── favicon.svg
│   └── fonts/
│
├── src/
│   ├── components/
│   │   ├── Head.astro
│   │   ├── blog/
│   │   │   ├── AuthorCard.astro
│   │   │   ├── BlogCard.astro
│   │   │   ├── BlogNavigation.astro
│   │   │   ├── FooterBlogCard.astro
│   │   │   ├── HeroBlogCard.astro
│   │   │   ├── NewsLatter.astro
│   │   │   ├── Pagination.astro
│   │   │   ├── RelatedBlogCard.astro
│   │   │   ├── StickyActionBar.astro
│   │   │   └── TagsFooter.astro
│   │   ├── home/
│   │   │   ├── BlogRow.astro
│   │   │   ├── FooterBlogRow.astro
│   │   │   ├── Hero.astro
│   │   │   └── PromoCard.astro
│   │   └── shared/
│   │       ├── Footer.astro
│   │       └── Header.astro
│   │
│   ├── layouts/
│   │   ├── BlogLayout.astro
│   │   └── Layout.astro
│   │
│   ├── pages/
│   │   ├── index.astro
│   │   ├── [slug].astro
│   │   └── post/
│   │       ├── index.astro
│   │       ├── [slug].astro
│   │       └── [page].astro
│   │
│   ├── styles/
│   │   └── global.css
│   │
│   ├── constants.ts          # Site configuration
│   └── content.config.ts     # AstraCMS content loader
│
├── .gitignore
├── .prettierrc.mjs
├── astro.config.mjs
├── eslint.config.js
├── tsconfig.json
├── package.json
├── LICENSE
└── README.md
```

## Configuration

All site settings are centralized in `src/constants.ts`. Edit this file to customize:

```typescript
// Site Information
export const SITE_NAME = "SkyScript";
export const SITE_TITLE = "The Sky Script Blog";
export const SITE_DESCRIPTION = "Your site description";
export const SITE_URL = "https://skyscript.com";

// SEO & Meta Tags
export const META_TITLE_TEMPLATE = "%s | SkyScript";
export const META_AUTHOR = "SkyScript Team";
export const META_KEYWORDS = ["cloud", "developers", "blog"];

// Open Graph / Social
export const OG_IMAGE = "/og-image.png";
export const TWITTER_SITE = "@skyscript";

// Footer Configuration
export const FOOTER_NAV_LINKS = [
  /* ... */
];
export const SOCIAL_LINKS = { facebook: "#", twitter: "#" /* ... */ };
```

## Tech Stack

- [Astro v5](https://astro.build) - Static site generator
- [AstraCMS](https://astracms.dev) - Headless CMS
- [TypeScript](https://www.typescriptlang.org/) - Typed JavaScript
- [Tailwind CSS v4](https://tailwindcss.com/) - Utility-first CSS
- [ESLint](https://eslint.org/) & [Prettier](https://prettier.io/) - Code quality

## Installation

```bash
# Clone the project
git clone <repository-url>
cd skyscript

# Install dependencies
pnpm install

# Set up environment variables
cp .env.example .env
# Add your ASTRACMS_API_KEY to .env

# Start development server
pnpm dev
```

The site will be available at `http://localhost:4321`

## Commands

| Command        | Description                        |
| -------------- | ---------------------------------- |
| `pnpm dev`     | Start local development server     |
| `pnpm build`   | Build production-ready static site |
| `pnpm preview` | Preview production build locally   |
| `pnpm lint`    | Lint code with ESLint              |
| `pnpm format`  | Format code with Prettier          |
| `pnpm sync`    | Sync Astro content types           |

## License

This project is open source. See [LICENSE](LICENSE) for more information.
