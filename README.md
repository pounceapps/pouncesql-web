# pouncesql-web

Static marketing + docs site for **pouncesql.com** (and `www.` / `pouncesql.senzall.com`).

Deployed as a Cloudflare **Worker (static assets)** named `pouncesql-web` via
**Workers Builds** — Cloudflare is connected to this GitHub repo and deploys on
every push to `main`. There is intentionally **no GitHub Actions deploy
workflow** and no Cloudflare token in GitHub.

- Site content lives in `public/`.
- Worker config is `wrangler.jsonc` (`assets.directory = ./public`).
- Custom domains are attached in the Cloudflare dashboard (Workers &amp; Pages →
  pouncesql-web → Settings → Domains &amp; Routes).

Local preview: `npx wrangler dev`.
