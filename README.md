# tangohost-website

Static site (plain HTML/CSS/JS, no build step) for Connectango.

## Hosting on GitHub Pages

One-time setup, done from the GitHub UI (requires repo admin access):

1. Go to `github.com/OpenTangoOrg/tangohost-website` → **Settings** → **Pages**.
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.
3. Branch: **main**, folder: **/ (root)** → **Save**.
4. After a minute or two it's live at `https://opentangoorg.github.io/tangohost-website/`.

`.nojekyll` is committed at the repo root so GitHub Pages serves the
site as-is instead of running it through Jekyll.

All internal links in the site use relative paths (no leading `/`), so
it works correctly whether it's served from the root of a custom
domain or from the `/tangohost-website/` subpath of the default
`github.io` URL.

### Adding the custom domain (connectango.org)

Once the domain is purchased, point it at this site:

1. Add a file named `CNAME` (no extension) at the repo root containing
   just the domain, e.g. `connectango.org`.
2. In your DNS provider for `connectango.org`, add the records GitHub
   requires:
   - For an apex domain (`connectango.org`): four `A` records pointing
     at GitHub Pages' IPs — `185.199.108.153`, `185.199.109.153`,
     `185.199.110.153`, `185.199.111.153`.
   - For a `www` subdomain: a `CNAME` record pointing at
     `opentangoorg.github.io`.
3. Back in **Settings** → **Pages**, enter `connectango.org` under
   **Custom domain** and save — GitHub will verify DNS and can
   auto-provision HTTPS once it resolves.

See GitHub's own docs for the current details:
https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site
