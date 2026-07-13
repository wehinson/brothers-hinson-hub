# The Brothers Hinson — Game Development (hub)

A single, self-contained landing page (`index.html`, no build step, no dependencies) that links to
our three browser games hosted on GitHub Pages.

## Links it points to
| Card | Repo | GitHub Pages URL |
|------|------|------------------|
| AbioGenesis | `wehinson/IdleLife`  | https://wehinson.github.io/IdleLife/ |
| Sweeper Inc. | `wehinson/IdleSweeo` | https://wehinson.github.io/IdleSweeo/ |
| Snake Forever | `wehinson/IdleSnake` | https://wehinson.github.io/IdleSnake/ |

> Update the `href`s in `index.html` if any repo name or Pages URL differs. Each game must have
> GitHub Pages enabled (repo → Settings → Pages) for its link to resolve.

## Deploy to Cloudflare Pages
This is a plain static site — no framework, no build.

**Option A — connect a Git repo (recommended):**
1. Push this folder to a GitHub repo.
2. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**.
3. Pick the repo. Build command: *(leave empty)*. Build output directory: `/` (root).
4. Deploy. Add a custom domain under the project's **Custom domains** tab if desired.

**Option B — direct upload (no Git):**
1. Cloudflare dashboard → **Workers & Pages** → **Create** → **Pages** → **Upload assets**.
2. Drag in `index.html` (and this README if you like). Deploy.

**Option C — Wrangler CLI:**
```
npx wrangler pages deploy . --project-name brothers-hinson
```

## Local preview
Any static server works, e.g. from this folder:
```
npx serve .
```
Then open the printed `localhost` URL.
