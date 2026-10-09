# davidmukka.com

Static site served by a Cloudflare Worker (static assets only, no server code).

```
public/          # everything that gets deployed
  index.html
  _headers       # security + cache headers
  images/
wrangler.jsonc   # Worker config
```

## Develop

```bash
npm install
npm run dev        # http://localhost:8787
```

## Deploy

Every push to `main` is built and deployed by Cloudflare Workers Builds
(the repo is connected in the Cloudflare dashboard under the `davidmukka-com`
Worker → Settings → Build).

