# Netlify SPA Kit (Drop‑in)

Deploy a single‑page app (SPA) or a standalone HTML file to Netlify in minutes.

## What’s inside
- `netlify.toml` — tells Netlify to publish the `public/` folder and rewrite all routes to your main HTML.
- `public/scrum_board.html` — placeholder. Replace with **your** real file.
- `public/_redirects` — same SPA fallback; also enables **Drag & Drop** deploys.
- `package.json` — optional CLI scripts for local testing & one‑command deploys.
- `.gitignore` — keeps `node_modules` out of Git if you install the CLI locally.

## Quick start (choose one)

### A) Git connect (zero build)
1. Replace `public/scrum_board.html` with your real file.
2. Commit + push to GitHub/GitLab/Bitbucket.
3. On Netlify: **New Site from Git** → pick this repo.
4. Ensure **Publish directory** is `public`. (UI or read from `netlify.toml`)
5. Deploy.

### B) Drag & Drop
1. Put your file into `public/scrum_board.html` (keep `_redirects` in the same folder).
2. Zip the **contents of `public/`** (not the parent folder).
3. On Netlify → **Sites** → **Add new site** → **Deploy manually** → Drop the zip/folder.

### C) CLI (one command)
```bash
# Optional: install the Netlify CLI locally
npm i -D netlify-cli

# Preview deploy (gets a temporary URL)
npm run deploy:preview

# Production deploy (needs first-time site linking)
npm run deploy
```
> On the first deploy with CLI, you'll be prompted to link/create a site.

## Notes
- If you keep your HTML file named `scrum_board.html`, this kit already routes `/` and any `/path` to it.
- If you rename your main file to `index.html`, you can remove the redirects from `netlify.toml` and delete `_redirects`.
- For SPA routing to work, **do not remove** the rewrite rules (unless you rename to `index.html`).

Enjoy!