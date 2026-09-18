# TypeSafe Docs

Traditional Chinese replica of the TypeSafe documentation site.

## Local preview

```bash
python3 -m http.server 4173
```

Open <http://127.0.0.1:4173>.

## Cloudflare Pages

This project is configured for Wrangler with `pages_build_output_dir = "."`.

```bash
npx wrangler pages project create typesafe-docs
npx wrangler pages deploy . --project-name typesafe-docs
```
