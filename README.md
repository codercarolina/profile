# carolynpierce.com

Personal professional site. Static — no build step.

## Deploy on GitHub Pages (one-time setup)

1. Create a new GitHub repository (e.g. `carolynpierce.com` — any name works; public repo required on the free plan for Pages).
2. Upload everything in this folder to the repository root: `index.html`, `headshot.jpg`, `headshot-social.jpg`, `favicon.png`, `CNAME`, `README.md`.
3. Repo → Settings → Pages → "Deploy from a branch" → Branch: `main`, folder `/ (root)` → Save.
4. The `CNAME` file tells Pages the custom domain. Confirm it appears in Settings → Pages → Custom domain, and check "Enforce HTTPS" once the certificate is issued (a few minutes).
5. At GoDaddy → your domain → DNS: remove the existing forwarding rule, then add:
   - Four **A records** for host `@`: `185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`
   - One **CNAME record**: host `www` → `YOUR-GITHUB-USERNAME.github.io`
6. DNS can take up to an hour. Verify at https://carolynpierce.com.

## Updating the site

Edit `index.html` in the repo (GitHub's web editor is fine) and commit — Pages redeploys automatically in ~1 minute.

**Scheduled edit — October 1, 2026:** change "Partner & CTO" phrasing to "Former Partner & CTO" (pill in the hero, timeline entry, and the JSON-LD `jobTitle`).
