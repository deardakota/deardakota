# Dear Dakota

Dear Dakota is a small personal placeholder website backed by GitHub and deployed through the existing Traefik + Cloudflare setup.

## Live update flow

1. Edit files in this repo.
2. Commit changes to `main`.
3. Push to GitHub.
4. The live server pulls the update automatically.

## Current files

- `index.html` — homepage
- `styles.css` — site styling
- `README.md` — repo overview
- `DEPLOYMENT.md` — deployment notes

## Local edit loop

```bash
git status
git add .
git commit -m "Describe change"
git push
```

## Notes

- The live site is already behind Traefik.
- Cloudflare is configured for Full Strict TLS.
- This repo is the source of truth for the site.
