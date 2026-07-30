# Deployment Notes

This site uses a simple push-to-git workflow.

## Current deployment model

- GitHub repo: `https://github.com/deardakota/deardakota.git`
- Live server: polls the repo every 60 seconds
- Reverse proxy: Traefik
- TLS: Cloudflare Full Strict

## Update process

1. Make changes locally in the repo.
2. Commit to `main`.
3. Push to GitHub.
4. Wait for the server poll to pull the latest commit.

## Safe update habits

- Keep `main` deployable.
- Avoid force-pushing unless absolutely necessary.
- Use small commits so rollbacks are easy.
- If a change looks risky, test it in a separate branch first.

## Quick commands

```bash
git add .
git commit -m "Update site"
git push
```

## When the site should change

If the homepage or assets do not update after a push, check:

- the repo received the commit
- the server pull loop is still running
- Traefik is routing the expected hostname
- Cloudflare DNS still points at the correct origin
