# TypeSafe Docs

Traditional Chinese replica of the TypeSafe documentation site.

## Local preview

```bash
python3 -m http.server 4173
```

Open <http://127.0.0.1:4173>.

## Cloudflare Pages

This is a static Cloudflare Pages site and intentionally has no Wrangler configuration file. In Cloudflare Pages project settings, leave the build command empty and set the build output directory to `.`. Do not add a custom deploy command; Pages performs the deployment itself.

The `CLOUDFLARE_API_TOKEN` used by the Pages build must be a token created for the account that owns the Pages project, with Pages project read/write permission (and account read permission). A token can authenticate successfully but still return API error `10000` when it lacks the Pages permission. Pages configuration does not accept `account_id` in `wrangler.toml`.

For a manual deployment outside the Pages Git integration, use:

```bash
npx wrangler pages deploy . --project-name typesafe-docs
```

Create the Pages project once with:

```bash
npx wrangler pages project create typesafe-docs --production-branch main --force
```
