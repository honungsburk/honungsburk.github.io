# Frank Hampus Weslien - Personal Blog

Personal blog and portfolio of Frank Hampus Weslien. Posts cover programming, technology, and other topics of interest. The goal is to showcase work and build a personal brand.

## Tech Stack

- **Static site generator**: [Zola](https://www.getzola.org/)
- **Hosting**: GitHub Pages
- **Custom domain**: frankhampusweslien.com

## Site Structure

- `/posts` — Blog posts (`content/posts/`)
- `/projects` — Project showcase (`content/projects/`)
- `/cv` — Curriculum vitae (`content/curriculum-vitae/`)

## Key Files

- `config.toml` — Zola site configuration
- `content/` — All markdown content
- `templates/` — Zola HTML templates
- `sass/` — Stylesheets
- `static/` — Static assets (images, etc.)

## Agent Purpose

Help write and publish new blog posts, update projects, and perform other site maintenance tasks. When creating new posts, follow the existing front matter conventions in `content/posts/`.

## Workflow

- Build the site locally: `zola build`
- Serve locally with live reload: `zola serve`
- New posts go in `content/posts/` as `.md` files with Zola front matter
