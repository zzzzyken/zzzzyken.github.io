# zzzzyken.github.io

Source of [zzzzyken.github.io](https://zzzzyken.github.io), the personal website of Ziyang Zhang. It is built with
[Jekyll](https://jekyllrb.com/) and the [al-folio](https://github.com/alshedivat/al-folio) starter (v1.x).

## Where things are

| To change                               | Edit                                                                                                |
| --------------------------------------- | --------------------------------------------------------------------------------------------------- |
| Home page text, subtitle, photo         | `_pages/about.md` (photo: `assets/img/prof_pic.jpg`)                                                |
| Publications                            | `_bibliography/papers.bib` (PDFs in `assets/pdf/`, thumbnails in `assets/img/publication_preview/`) |
| Web CV                                  | `_data/cv.yml`                                                                                      |
| CV PDF                                  | replace `assets/pdf/Ziyang_Zhang_CV.pdf`                                                            |
| Email, GitHub and other profile links   | `_data/socials.yml`                                                                                 |
| Links on co-author names                | `_data/coauthors.yml`                                                                               |
| Name, site description, feature toggles | `_config.yml`                                                                                       |
| News items on the home page             | add files to `_news/` and set `announcements.enabled: true` in `_pages/about.md`                    |

Template documentation: [`docs/CUSTOMIZE.md`](docs/CUSTOMIZE.md), [`docs/FAQ.md`](docs/FAQ.md).

## Deployment

Every push to `main` runs the "Deploy site" workflow, which builds the site and publishes it to the `gh-pages` branch.
GitHub Pages serves that branch (Settings, Pages, "Deploy from a branch", `gh-pages`).

## Local preview

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

Ruby 3.3 is required; ImageMagick (`convert`) is used for responsive images.

## License

The site is based on al-folio, which is released under the MIT License (see [`LICENSE`](LICENSE)).
