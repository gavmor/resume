# résumé

Gavin N. Morgan's résumé, kept as source and built by CI.

- **Source:** [`resume.html`](resume.html) — single self-contained HTML file,
  designed print-first (US Letter, 2 pages).
- **Build:** every push to `main` renders
  [`dist/Gavin-Morgan-Resume.pdf`](dist/Gavin-Morgan-Resume.pdf) with
  [WeasyPrint](https://weasyprint.org/) and cuts a semver GitHub release
  carrying the PDF. See [`.github/workflows/build.yml`](.github/workflows/build.yml).
- **Manual release:** Actions → *Build and release resume PDF* → *Run workflow*,
  choosing the `patch`/`minor`/`major` bump.

## Local build

```sh
pip install weasyprint
weasyprint resume.html dist/Gavin-Morgan-Resume.pdf
```

(WeasyPrint also needs Pango: `libpango-1.0-0` and `libpangoft2-1.0-0`.)
