# gunahn.github.io

Personal academic website of **Gun Ahn**, PhD candidate, MIT Brain and Cognitive Sciences.
Live at <https://gunahn.github.io>.

Plain static HTML and CSS. No build step, no dependencies, no Jekyll. GitHub Pages serves the
files exactly as they are in this repository (that's what the empty `.nojekyll` file is for).

## Layout

| File | Page |
| --- | --- |
| `index.html` | About: intro, education, publications, honors, skills |
| `research.html` | Research & Projects |
| `outreach.html` | STEM Outreach: STEM Vision Scholarship |
| `books.html` | My Books |
| `faq.html` | MIT BCS PhD Application FAQ |
| `404.html` | Not-found page |
| `assets/style.css` | All styling (light + dark theme via CSS custom properties) |
| `assets/img/` | Portrait, research figures, book covers |

## Editing

Open the relevant `.html` file and edit the text directly. The markup is plain and commented by
structure. Each page repeats the same `<nav>` and `<footer>` blocks, so **if you change a nav link
or a contact link, change it in all six pages**.

Common edits:

- **Add a publication**: copy an existing `<li>` inside `<ol class="pubs">` in `index.html`.
  Wrap your own name in `<span class="me">Ahn, G.</span>`; add `<a class="tag" …>` chips for
  Code / Paper / News links.
- **Add a research project**: copy an `<article class="proj">` block in `research.html`.
- **Add a book**: copy an `<article class="book">` block in `books.html`.
- **Add an FAQ entry**: copy a `<details>` block in `faq.html`.
- **Change colors**: edit the `--accent` / `--bg` / `--fg` custom properties at the top of
  `assets/style.css`. Each one is defined three times: light, `prefers-color-scheme: dark`, and
  an explicit `[data-theme="dark"]` override. Change all three.

## Preview locally

```bash
python3 -m http.server 8899
```

Then open <http://localhost:8899>.

## Deploy

Push to `master`. GitHub Pages rebuilds within about a minute.

```bash
git add -A && git commit -m "Update content" && git push
```

## History

The `archive/minimal-mistakes-2021` branch holds the previous, unused fork of the
Minimal Mistakes Jekyll theme that lived here before this site.
