# TypeSafe Docs

Traditional Chinese replica of the TypeSafe documentation site.

## Local preview

```bash
python3 -m http.server 4173
```

Open <http://127.0.0.1:4173>.

## Cloudflare Pages

This project is configured for Wrangler with `pages_build_output_dir = "."`.

In Cloudflare Pages project settings, leave the build command empty and set the build output directory to `.`. Do not use `npx wrangler deploy`, which is the Workers command.

If a deploy command is required, use the Pages command:

```bash
npx wrangler pages deploy . --project-name typesafe-docs
```

Create the Pages project once with:

```bash
npx wrangler pages project create typesafe-docs --production-branch main --force
```
