# Astro + Cloudflare

This is simple demo application to show deploying an Astro site via a Cloudflare Worker.
The content of the site is simply the `with-mdx` template from Astro followed by small tweaks to deploy to Cloudflare
Worker via a GitHub Actions workflow.

- Astro initialized via `pnpm create astro hello-astro -- --add cloudflare --skip-houston --install --template with-mdx`.
- The `package.json` script was modified to generate Cloudflare types (i.e. `wrangler types`).
- The `@astrojs/cloudflare` integration was added via `astro.config.mjs`.
- The deployment workflow is in `.github/workflows/build_and_deploy.yml`.
    - The resulting URL is https://hello-astro-cloudflare.colby-white.workers.dev.
