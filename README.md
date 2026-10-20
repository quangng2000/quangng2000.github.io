# Quang Nguyen

Personal website for ML research, built with [al-folio v1.2](https://github.com/alshedivat/al-folio/releases/tag/v1.2) and Jekyll.

**Website:** <https://quangng2000.github.io>

## Edit your website

| Content                                   | File                       |
| ----------------------------------------- | -------------------------- |
| Name, description, and site settings      | `_config.yml`              |
| Homepage biography and research interests | `_pages/about.md`          |
| Project pages                             | `_projects/*.md`           |
| GitHub and other social links             | `_data/socials.yml`        |
| Publication entries, when ready           | `_bibliography/papers.bib` |
| Photos and other images                   | `assets/img/`              |

You can edit these files directly on GitHub using the pencil button. Commit to `main` to build and publish automatically. The Actions tab shows build and deployment status.

The site currently has About and Projects pages. Sample publications, CV details, contacts, and posts have been removed. Add your own before enabling those sections.

Homepage and Projects entries use descriptions, preview images, and links from each project's front matter. Image provenance is recorded in `assets/img/research/SOURCES.md`.

The compact layout, IBM Plex typography, navy links, and illustrated project rows follow the supplied Dat Nguyen reference site. `assets/css/_research.scss` contains site-specific styling. `assets/css/main.scss` retains the pinned al-folio imports and loads those styles; this intentional override is tracked in `.al-folio-overrides.yml`.

## Deployment

Settings → Pages → Source is set to **GitHub Actions**.

`.github/workflows/deploy.yml` builds Jekyll with the dependencies pinned in `Gemfile.lock`, checks the intentional stylesheet override, and uploads the generated `_site` directory. Only `main` deploys to GitHub Pages. Pull requests and manually dispatched feature branches build without publishing.

The username site requires `url: https://quangng2000.github.io` and `baseurl: ""`.

## Local preview

With Docker running:

```sh
docker compose up
```

Open <http://localhost:8080/>. Alternatively, with Ruby 3.3.5 and Bundler installed, run `bundle install`, `npm ci`, then `bundle exec jekyll serve`.

## Template

The site retains the al-folio MIT license and footer attribution. Upstream setup and customization guides are in `docs/`.
