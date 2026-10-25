# Daily routine prompt — add one SEO micro-tool page

Use this text as the body of a recurring routine / scheduled agent task. Goal: grow the static site by **one new tool page per day** with almost no ops from the owner.

---

## Prompt (copy below)

```
You are maintaining the static site at /workspace/seo-micro-tools/ (or the cloned repo root).

Daily job — do all of this without asking the owner questions:

1. Read BACKLOG.json. Pick the first item where status is "todo". If none remain, stop and report “backlog empty”.
2. Create tools/<slug>.html as a complete one-page tool:
   - Match the look of existing tools (shared ../assets/style.css, header, breadcrumb, ad-slot, FAQ, footer).
   - Unique <title>, meta description, H1 based on the keyword/title.
   - FAQ section (3 Q&As) + matching FAQPage JSON-LD.
   - Vanilla JS only; tool must actually work offline after load; no backend; no external API calls unless strictly needed for the tool concept (prefer pure client-side).
   - Include Copy (and Clear when useful) buttons.
3. Add a card on index.html linking to the new tool (title + one-line blurb).
4. In BACKLOG.json set that item's status to "done" and add "shipped": "YYYY-MM-DD" (owner timezone Asia/Shanghai).
5. Do not register domains, deploy externally, or claim revenue. Do not ask the owner for input.
6. Report back: tool name, file path, and remaining todo count.
```

---

## Schedule suggestion

- Cadence: daily (e.g. 09:00 Asia/Shanghai)
- Trigger: calendar / cron / Grok Bot routine
- Stop condition: backlog empty, or owner pauses the routine

## After the agent finishes

Owner (or CI) only needs: `git add -A && git commit -m "Add <tool>" && git push` so Vercel/GitHub Pages redeploys. If the repo is already connected, that push is the only ops step — or skip git and re-upload the folder manually.
