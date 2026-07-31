# Personal academic page with Jekyll

This is the start of a personal academic page build with Jekyll. The goal is to use the theme [Minimal Mistakes](https://mmistakes.github.io/minimal-mistakes/) and customize it to my needs. The page will be hosted on GitHub Pages and will contain information about my profile, history, publications, and other relevant information. In summary, it will be my academic CV.

## Previous page

I already have a personal page hosted on GitHub Pages using Wowchemy, now HugoBlox. The page is available at [https://josecoliveira.github.io](https://josecoliveira.github.io). However, I want to have more control over the page and its content, so I decided to create a new page using Jekyll. Also, the new HugoBlox theme is bloated and not very customizable. I still want to use a tool that generates static pages, so I decided to use Jekyll as a middle ground between pure coding and hard page builders.

## Expected features

The first page will be a copy of [Ramon Gonze](ramongonze.github.io)'s page, which is a good example of a personal academic page. The page will contain the following sections:

- Left side bar with picture, name, title, location, email, and links.
- Main body with sections for:
  - About me (bio)
  - Publications
  - Software
- About me page:
  - Extended bio
  - Experience section
  - Education section

I also want to publish a page with guidelines for teaching assistants to be used by my old supervisor new teaching assistants. I do not have knowledge on how Jekyll works as this is my first time using it, so we will leave the page for later. I do not plan to use this page as a blog with regular posts, but I want to use it to have pages with information that might be useful for my students and collaborators.

## Current status

> Update this section as the project progresses.

### Completed (2026-07-30)

The site is fully built with real content, configured for GitHub Pages, and running locally.

### Completed (2026-07-31 — Final setup)

#### Configuration
- **`_config.yml`**: Uses `remote_theme: "mmistakes/minimal-mistakes@4.28.0"` (GitHub Pages compatible). Site title: "José C. Oliveira", email: josecarlosdeoliveirajr@gmail.com, location: L'Aquila, Italy.
- **Gemfile**: Uses plain `jekyll` (4.4.x) **instead of the `github-pages` gem** (which pins Jekyll 3.9/Liquid 4.0.3 and breaks on Ruby 4). **Liquid is explicitly pinned `~> 4.0.4`** (4.0.4 removed the `tainted?`/`untaint` calls — 4.0.3 still has them and fails on Ruby 4). Includes `jekyll-remote-theme`, `jekyll-include-cache`, `jekyll-paginate`, `jekyll-sitemap`, `jekyll-gist`, `jemoji`, plus Ruby 4.0 compat gems (`csv`, `webrick`, `bigdecimal`, `faraday-retry`).
- **Author sidebar**: GitHub, ORCID (0009-0000-2266-0032), Google Scholar (gd98-_oAAAAJ) icons. No website, email, or Twitter.
- **Social preview**: Profile picture used as OG image.
- **MathJax**: LaTeX rendering enabled via CDN.

#### Pages
| Page | URL | Content |
|------|-----|---------|
| Home | `/` | Dynamic layout with About bio, Publications list, Projects list |
| Publications | `/publications/` | Full list with links to detail pages |
| Projects | `/projects/` | Full list with descriptions and links |
| Teaching | `/teaching/` | TA history with course tables (UMD + UFMG) |
| TA Guide | `/teaching/ta-guide/` | Full TA Excellence Guide for Automata & Formal Languages |
| About | `/about/` | Bio, interests, 5 experience entries, 3 education entries |

#### Structure
- **`_layouts/home.html`** — Custom homepage layout (adapted from Ramon Gonze's design)
- **`_publications/`** — Collection (thesis.md, esslli22.md) with BibTeX files in `assets/bib/`
- **`_projects/`** — Collection (kg2.md, akvmodel.md)
- **`_pages/`** — Static pages (about.md, publications.md, projects.md, teaching.md, ta-guide.md)
- **`_data/navigation.yml`** — Navigation: Home, Publications, Projects, Teaching, About
- **`_includes/head/custom.html`** — Custom CSS (avatar size, font reduction) + MathJax

#### Local Development
- Site runs at `http://127.0.0.1:4000`
- Serve command: `bundle exec jekyll serve`
- Build command: `bundle exec jekyll build`
- Ruby 4 works out of the box — **no monkey-patch needed** with Jekyll 4.4.

### Completed (2026-07-31 — GitHub Actions deployment)

- **Deployment**: Replaced GitHub Pages' built-in Jekyll builder with a **GitHub Actions** workflow (`.github/workflows/jekyll.yml`).
  - Builds on `ubuntu-latest` with **Ruby 4.0** (matches local Ruby 4.0.6), runs `bundle exec jekyll build`, uploads the `_site` artifact, and deploys via `actions/deploy-pages`.
  - `Gemfile.lock` includes `ruby` and `x86_64-linux` platforms so `bundler-cache: true` works on the Linux runner.
- **Why**: GitHub Pages' built-in builder pins an old Ruby/Liquid and ignores `_plugins/`. GitHub Actions gives full control over the Ruby version and matches local development.
- **Ruby 4**: Jekyll 4.4 + **Liquid ~> 4.0.4** (which removed `tainted?`) means **no monkey-patch is needed** locally or in CI. ⚠️ Trap: Jekyll auto-loads every `_plugins/*.rb`, so an old `_plugins/ruby34_compat.rb` silently masked Liquid 4.0.3 — the Liquid pin is what actually fixes Ruby 4, not any plugin.
- **Deploy steps**: Push to `main` → workflow builds & deploys. In repo Settings → Pages, set **Source: GitHub Actions**.
- **Sass warnings**: Dart Sass prints deprecation warnings from the Minimal Mistakes theme's Sass (`@import`, `mix()`, etc.). Harmless — CSS builds correctly. (Optional future cleanup: silence or update theme Sass.)

#### Notes
- Profile picture was copied from old HugoBlox site; consider a fresh high-quality headshot.
- Feature row / splash images are intentionally not used (clean text-based layout).
- CV intentionally omitted — CVs should be tailored per application.
