# Golnoosh Profile

Static profile and promo site for Golnoosh.

## Live Site

- Production domain: <https://golnoosh.nooshline.nl/>
- Hosted as a subdomain under `nooshline.nl`, but this is a standalone personal profile.

## Current Source Notes

The profile copy is synthesized from the CV files in `CV/`, with multidisciplinary project coordination and PMO
support as the leading angle and ESG/sustainability, supply chain planning, smart mobility, urban research, transport
coordination, system dynamics, founder-led ecommerce, sales support, customer operations, project planner and
cover-letter variants as supporting evidence.
Private address, phone and email details from the CVs are intentionally not published on the website. Public contact
routing is limited to LinkedIn.

Nooshline and Oran-Je are referenced as founder/co-founder proof for entrepreneurship, product judgment, ecommerce
operations and customer awareness. They support the personal profile; they are not the subject or visual identity of
the site.

## SEO and Legal Surface

- `index.html` is the canonical, indexable profile page.
- `sitemap.xml` lists the profile, legal pages and important profile images.
- `robots.txt` allows crawling and points crawlers to the sitemap.
- `privacy.html`, `terms.html` and `accessibility.html` are linked from the footer and marked `index,follow`.
- `llms.txt` provides a compact machine-readable profile summary for AI and agent crawlers.
- Simple Analytics is included with JavaScript and noscript fallbacks for cookie-free, anonymous aggregate traffic statistics.
- Root favicon assets and `site.webmanifest` provide stable search/browser icon signals.

## Deployment

This is a static GitHub Pages site. GitHub Pages is configured to publish from the `main` branch root, so pushes to
`main` update production.

The `CNAME` file sets the custom domain to:

```text
golnoosh.nooshline.nl
```

For DNS, create a CNAME record for `golnoosh` under `nooshline.nl` pointing to:

```text
shoopi.github.io
```

Then enable/enforce HTTPS in GitHub Pages after DNS resolves. Do not upload this into the Nooshline WooCommerce theme
unless the subdomain is intentionally routed through WordPress.

Important privacy boundary: do not publish the `CV/` source folder as a browsable public directory. The included
`.gitignore` excludes `CV/` from the GitHub repo, so the source CV documents stay local and out of production.

## Local Preview

Open `index.html` directly in a browser, or run:

```bash
python3 -m http.server 4173
```

Then visit <http://localhost:4173/>.
