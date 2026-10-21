# Wen Research Group website

Quarto sources for [jaywen.com](https://jaywen.com).

## Content

- `education.qmd`: public courses and learning modules, including the IAMG 2026 river chemistry and deep learning module. Its thematic illustration is `assets/artworks/iamg-2026-river-chemistry.png`.
- `people.qmd`: current team members and alumni. Current members omit group start dates; undergraduates may list their expected degree and class year. Alumni list a degree with its graduation year (marked expected where applicable) or a group role with its dates. Approved portraits are stored in `files/portraits/`. All People cards, including the PI, use equal-width columns: three on desktop, two at 760px and below, and one at 520px and below.
- Portraits in `people.qmd` use `fig-alt` for accessible names without visible captions; each card shows its name only in the heading.
- `publication.qmd`: journal articles, chapters, reports, preprints, and open datasets and code. Keep publication status and author annotations consistent with the reviewed CV. Match local PDFs in `files/papers/` to the article title and DOI before adding PDF buttons.
- `files/Tao_Wen_CV.pdf`: the public CV linked from Contact. Replace it only with the verified `Tao_Wen_CV_Public.pdf` from the CV project; pending grants must be omitted while funded grants and other content are retained.
- `_quarto.yml`: site navigation, shared appearance, and output settings.

## Preview and verify

Install Quarto, then preview the site from the repository root:

```sh
quarto preview
```

Render changed pages individually with `quarto render <page>.qmd`, or build the complete site with `quarto render`. Check the rendered pages in a browser and run `git diff --check` before publishing. Generated output in `_site/` is ignored by Git.

Before replacing the public CV, run the CV project's read-only `python3 -B scripts/release_check.py` check to verify the full/public editions differ only by the pending-grant section and page footers. Keep the website filename unchanged so existing CV links remain valid.

## Publish

Pushing to `main` starts the **Quarto Publish** workflow in `.github/workflows/publish.yml`. It renders the site and publishes the output to `gh-pages`, which GitHub Pages serves at [jaywen.com](https://jaywen.com).

After pushing, verify both **Quarto Publish** and **pages build and deployment** succeed, then check the changed pages on the live site. Include new portrait files in the source commit.
