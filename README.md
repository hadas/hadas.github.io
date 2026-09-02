# hadas.github.io

Personal academic website of Hadas Raviv — https://hadas.github.io/

Hand-written static HTML and CSS.

## Layout

```
index.html          About (landing page)
publications.html   Papers in review + published
talks.html          Invited talks, conference talks, posters
cv.html             Full CV
404.html            Not-found page
css/style.css       The entire stylesheet
assets/             Logos, portrait, favicon
.nojekyll           Serve files as-is; skip GitHub's Jekyll build
robots.txt
sitemap.xml
```

## Editing

Every page is a complete, self-contained HTML document. The `<header>` and
`<footer>` blocks are intentionally duplicated across the four pages — that is
the cost of having no build step. When you change one, change all four; they are
byte-identical apart from the `aria-current="page"` marker on the active tab, so
a find-and-replace across `*.html` works.

## Assets

`assets/` currently holds neutral **placeholders** so nothing renders broken.

## Local preview

```sh
python3 -m http.server 8000 --directory .
# then open http://localhost:8000
```

Opening the files directly with `file://` works too, but `404.html` and the
root-relative paths in it only behave correctly over HTTP.

## Publishing

GitHub Pages serves a repository named `<username>.github.io` from the root of
its default branch, at `https://<username>.github.io/`. The repository must be
public (on a free plan). Settings → Pages → Source: *Deploy from a branch* →
`main` / `/ (root)`.
