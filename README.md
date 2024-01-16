# Shopify App Template - Remix

This is a template for building a [Shopify app](https://shopify.dev/docs/apps/getting-started) using the [Remix](https://remix.run) framework.

## Reproduce plugin-cloudflare postinstall script issue

1. make sure .npmrc includes `node-linker = hoisted` to force postinstalls scripts to re-run on every install (in order to force the failing line to run)
2. if you have not already run `pnpm i`
3. run `pnpm i` again after cloudflared has been downloaded to `node_modules/@shopify/plugin-cloudflare/bin/`
4. `node_modules/@shopify/plugin-cloudflare/scripts/postinstall.js` fails

Alternatively you can simply

1. cd `node_modules/@shopify/plugin-cloudflare`
2. run `pnpm postinstall`
