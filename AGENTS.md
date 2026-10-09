# Agent guidelines

## Git workflow

Never commit or push directly to `main`. Every push to `main` is deployed to
production by Cloudflare Workers Builds.

1. Create a branch from an up-to-date `main`:
   ```bash
   git checkout main && git pull
   git checkout -b <short-descriptive-name>
   ```
2. Commit your changes on that branch and push it:
   ```bash
   git push -u origin <short-descriptive-name>
   ```
3. Open a pull request against `main`:
   ```bash
   gh pr create --base main --fill
   ```
4. Leave the PR for review. Don't merge it yourself.
