# Wen Research Group website

Quarto sources for [jaywen.com](https://jaywen.com).

## Content

- `education.qmd`: public courses and learning modules, including the IAMG 2026 river chemistry and deep learning module.
- `people.qmd`: current team members and alumni. Approved portraits are stored in `files/portraits/`.
- `publication.qmd`: journal articles, chapters, reports, preprints, and open datasets and code. Keep publication status and author annotations consistent with the reviewed CV.
- `_quarto.yml`: site navigation, shared appearance, and output settings.

## Preview and verify

Install Quarto, then preview the site from the repository root:

```sh
quarto preview
```

Render changed pages individually with `quarto render <page>.qmd`, or build the complete site with `quarto render`. Check the rendered pages in a browser and run `git diff --check` before publishing. Generated output in `_site/` is ignored by Git.

## Publish

Pushing to `main` starts the **Quarto Publish** workflow in `.github/workflows/publish.yml`. It renders the site and publishes the output to `gh-pages`, which GitHub Pages serves at [jaywen.com](https://jaywen.com).

After pushing, verify both **Quarto Publish** and **pages build and deployment** succeed, then check the changed pages on the live site. Include new portrait files in the source commit.
