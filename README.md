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

The `CLOUDFLARE_API_TOKEN` used by the Pages build must be a token created for the account that owns the Pages project, with Pages project read/write permission (and account read permission). A token can authenticate successfully but still return API error `10000` when it lacks the Pages permission. Pages configuration does not accept `account_id` in `wrangler.toml`.

If a deploy command is required, use the Pages command:

```bash
npx wrangler pages deploy . --project-name typesafe-docs
```

Create the Pages project once with:

```bash
npx wrangler pages project create typesafe-docs --production-branch main --force
```
