# SEO Micro Tools (v1)

Boring, useful, client-side micro tools for SEO long-tail traffic. Static HTML/CSS/JS only — no backend, no build step.

## What's included

- `index.html` — hub listing all tools
- `tools/*.html` — one page per tool (10 tools in v1)
- `assets/style.css` — shared mobile-friendly styles
- `BACKLOG.json` — 20 more tool ideas for daily expansion
- `DAILY_ROUTINE.md` — prompt text for a future “add one tool per day” routine

All tools run with vanilla JavaScript in the browser. Nothing is uploaded.

## Deploy in 3 steps

### Option A — Vercel

1. Create a GitHub repo and push this folder (`seo-micro-tools/`) as the repo root (or set Root Directory to this folder).
2. Import the repo in [vercel.com](https://vercel.com) → Framework Preset: **Other** → Build Command empty → Output Directory: `.` (or leave default for static).
3. Deploy. Point a custom domain later in Project → Settings → Domains.

### Option B — GitHub Pages

1. Push this folder to a GitHub repo (e.g. `username/seo-micro-tools`).
2. Repo → Settings → Pages → Source: **Deploy from a branch** → Branch: `main` → Folder: `/ (root)`.
3. Save. Site will be at `https://username.github.io/seo-micro-tools/` (or a custom domain you add in Pages settings).

No Node build is required. Upload the HTML as-is.

## Daily page adds

1. Open `BACKLOG.json` and take the first item with `"status": "todo"`.
2. Copy an existing tool page under `tools/` as a template; change title, description, H1, FAQ, and the tool JS.
3. Add a card link on `index.html`, set the backlog item to `"done"`, commit, and redeploy (Vercel/Pages auto-deploy on push).

See `DAILY_ROUTINE.md` for a ready-made agent/routine prompt.

## Revenue honesty

This site does **not** make money by itself. Traffic from SEO is only half the loop.

To earn later you still need:

- A real domain (or keep free `*.vercel.app` / `*.github.io` while testing)
- Ad network approval (e.g. Google AdSense) and/or affiliate links in the footer ad slots
- Enough organic traffic for those slots to matter

Footer and mid-page “Advertisement placeholder” blocks are ready for ad snippets. Do not invent RPM/revenue claims until ads are live and measured.

## Local preview

```bash
cd /path/to/seo-micro-tools
python3 -m http.server 8765
# open http://127.0.0.1:8765/
```

## License

Use and modify freely for your own projects.
