# Source & Repository Tracking — dalesackrider-com

## Repository Information
- **Repository:** `https://github.com/dsackr/dalesackrider-com`
- **Primary Branch:** `main`
- **Production URL:** `https://dalesackrider.com`
- **Deployment Platform:** Cloudflare Pages
- **Framework:** Astro 5.4 + Tailwind CSS v4

## Key Directory Structure
```
dalesackrider-com/
├── .github/
│   └── workflows/
│       └── deploy.yml            # CI/CD auto-deployment workflow
├── public/                       # Static public assets (favicon, redirects)
├── src/
│   ├── components/
│   │   ├── BlogCard.astro        # Reusable blog card component
│   │   ├── Footer.astro          # Site footer with links & copyright
│   │   ├── FormattedDate.astro   # Date formatting component
│   │   ├── Header.astro          # Sticky navigation header
│   │   ├── Hero.astro            # Homepage executive hero banner
│   │   └── ThemeToggle.astro     # Dark/light mode switcher
│   ├── content/
│   │   └── blog/                 # Markdown blog posts
│   ├── layouts/
│   │   ├── BaseLayout.astro      # Core HTML layout & metadata
│   │   └── BlogPostLayout.astro  # Post template & author bio
│   ├── pages/
│   │   ├── 404.astro             # Custom 404 error page
│   │   ├── about.astro           # About page
│   │   ├── archive.astro         # Year-grouped post archive
│   │   ├── index.astro           # Homepage with Hero, Featured & Grid
│   │   ├── posts/
│   │   │   └── [slug].astro      # Dynamic blog post route
│   │   └── rss.xml.js            # RSS feed generator
│   └── styles/
│       └── global.css            # Tailwind & theme variables
├── astro.config.mjs              # Astro configuration
├── package.json                  # NPM dependencies & scripts
├── tailwind.config.mjs           # Tailwind configuration
├── tsconfig.json                 # TypeScript configuration
├── wrangler.jsonc                # Cloudflare Wrangler config (JSONC)
├── wrangler.toml                 # Cloudflare Wrangler config (TOML)
└── DEPLOYMENT.md                 # Deployment & setup documentation
```

## Branch Strategy & Workflow
1. Development occurs on feature branches or directly on `main` for publishing articles.
2. Every push to `main` triggers `.github/workflows/deploy.yml` which builds and deploys to Cloudflare Pages.
3. Content authors can add new posts directly to `src/content/blog/<slug>.md`.
