# Website editing guide

This is Quang Nguyen's personal ML research website, based on al-folio v1.2.

- Keep the name Quang Nguyen and site URL https://quangng2000.github.io unless the owner requests a change.
- This is a username GitHub Pages site: `_config.yml` must have `baseurl: ""`.
- Edit content in `_pages`, `_projects`, `_data`, and `_bibliography`; keep content factual and do not invent credentials, affiliations, publications, or contact information.
- Preserve the al-folio theme, its pinned gem dependencies, MIT license, and attribution.
- Runtime layouts and styles live in the `al_*` gems. `assets/css/main.scss` is an intentional, acknowledged override that preserves the gem imports and adds `assets/css/_research.scss`. Keep that acknowledgement current if the entrypoint changes.
- The homepage uses `layout: default` with a site-owned header and research sections. Both About and Projects render descriptions, illustrations, and links from `_projects` front matter. Keep project copy there to avoid drift.
- Sample publications, CV, blog, and profile imagery are intentionally absent. Add the owner's actual content before enabling these sections.
- GitHub Pages uses the native Actions deployment in `.github/workflows/deploy.yml`. Source lives on `main`; there is no generated `gh-pages` branch.

## Validation

Run `npm ci`, `npm run lint:prettier`, and `npm run lint:style-contract`. With Ruby 3.3.5 available, also run `bundle install`, `bundle exec al-folio upgrade audit --no-fail`, and `JEKYLL_ENV=production bundle exec jekyll build`. The GitHub Actions workflow runs the production build before deployment.

Check About, Projects, individual project pages, mobile navigation, and dark mode after visual changes. Upstream docs in `docs/` describe the original template; examples using `/al-folio` do not apply to this site's root URL.
