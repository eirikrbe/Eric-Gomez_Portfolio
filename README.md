# Eric Gómez — Developer Portfolio

Personal portfolio site of **Eric Gómez** — Electronics & Software Engineer, Master of Software Engineering candidate (Yoobee College, Auckland).

🔗 **Live:** https://eirikrbe.github.io/Eric-Gomez_Portfolio/

It presents a short bio, a filterable project grid, a visual tech stack, an experience timeline, and a downloadable CV. Content lives in plain Markdown/YAML, so the site is edited by changing data files rather than code.

## Tech stack

- [Hugo](https://gohugo.io/) (Extended) with the [HugoBlox](https://github.com/HugoBlox/kit) **dev-portfolio** theme, pulled in as a Hugo Module
- Tailwind CSS (via `@tailwindcss/cli`), built through Hugo's asset pipeline
- Deployed to **GitHub Pages** via GitHub Actions on every push to `main`

## Local development

Requires **Hugo Extended**, **Node.js 22+**, and **pnpm**.

```bash
# 1. Install the Node dependencies (Tailwind CLI, preact, etc.)
pnpm install

# 2. Run the dev server
hugo server
```

To reproduce a production build exactly as GitHub Pages does it (the site is served
from a subpath, so the base URL matters):

```bash
export PATH="$PWD/node_modules/.bin:$PATH"
hugo --minify --baseURL "https://eirikrbe.github.io/Eric-Gomez_Portfolio/"
```

## Where the content lives

| What | File |
| :--- | :--- |
| Homepage sections (hero, projects, tech stack, experience, contact, CTA) | `content/_index.md` |
| Profile data (name, role, bio, links, education, skills) | `data/authors/me.yaml` |
| Projects | `content/projects/<slug>/index.md` |
| Profile photo | `assets/media/authors/me.jpg` |
| Favicon | `assets/media/icon.svg` (with `icon.png` fallback) |
| Downloadable CV | `static/uploads/cv.pdf` |

A couple of theme-specific gotchas worth knowing:

- **Profile photo** is resolved by the author *slug*, not by any `avatar:` path — the
  file must be named `assets/media/authors/me.<ext>`.
- **Downloadable files** (like the CV) must live under `static/`, and links to them
  include the `/Eric-Gomez_Portfolio/` base path because the theme emits button hrefs raw.

## Deployment

Pushing to `main` triggers `.github/workflows/deploy.yml`, which builds the site with
Hugo and publishes it to GitHub Pages. No manual steps required.

## Credits

Built on the open-source [HugoBlox dev-portfolio](https://github.com/HugoBlox/hugo-theme-dev-portfolio)
theme. Theme code is MIT licensed by Lore Labs; site content © Eric Gómez.
