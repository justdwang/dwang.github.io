# justdwang.github.io

Academic personal homepage for Geneticode Lab, published with GitHub Pages and built from the AcadHomepage Jekyll template.

Site URL:

- https://dwang.net
- https://justdwang.github.io

## Project Structure

- `_config.yml`: site title, author profile, repository, SEO, and Jekyll settings
- `_pages/about.md`: homepage content
- `_data/navigation.yml`: top navigation links and page anchors
- `images/`: avatar, favicon, and image assets
- `assets/`, `_sass/`, `_includes/`, `_layouts/`: theme files from AcadHomepage
- `google_scholar_crawler/`: optional Google Scholar citation crawler
- `.github/workflows/google_scholar_crawler.yaml`: optional citation statistics workflow

## Editing The Homepage

Most content updates should be made in:

```text
_pages/about.md
```

The navigation bar uses in-page anchors. If you add a new section, add a matching anchor in `_pages/about.md` and a matching entry in `_data/navigation.yml`.

Example:

```html
<span class='anchor' id='research'></span>
<h1>Research</h1>
```

```yaml
- title: "Research"
  url: "#research"
```

## Publishing

This repository is intended to be used directly as a GitHub Pages repository. After editing:

```bash
git add .
git commit -m "Update homepage"
git push origin main
```

If the remote is named `justdwang` instead of `origin`, use:

```bash
git push justdwang main
```

## Local Preview Optional

Local preview is optional. GitHub Pages can build the site after pushing to GitHub.

If you want to preview locally:

```bash
bundle install
bundle exec jekyll serve
```

Then open:

```text
http://127.0.0.1:4000
```

If Bundler tries to install gems into the system Ruby directory, run:

```bash
bundle config set path 'vendor/bundle'
bundle install
```

## Google Scholar Citation Stats

The citation workflow is included from the template. It only runs usefully after configuring the repository secret:

```text
GOOGLE_SCHOLAR_ID
```

Without that secret, the homepage still works normally.

## Attribution

This site is based on [AcadHomepage](https://github.com/RayeRen/acad-homepage.github.io).
