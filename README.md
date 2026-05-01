# Personal website

Static Jekyll site. To **maintain** it, you almost never touch HTML or CSS — you just add or edit small markdown files.

## Daily maintenance — adding content

| To add a... | Create / edit |
|-------------|---------------|
| News item   | `_data/news.yml` (one block at the top) |
| Publication | `_publications/YYYY-MM-DD-shortname.md` |
| Talk        | `_talks/YYYY-MM-DD-shortname.md` |
| Course      | `_teaching/YYYY-shortname.md` |
| Anything in the About blurb | `index.html` (top section) |
| CV content  | `cv.html` |

Site-wide info (your name, affiliation, email, links) lives in **`_config.yml`**. Edit once, propagates everywhere.

## Frontmatter cheat-sheet

**Publication** — see `_publications/` for examples.
```yaml
---
title: "Paper Title"
section: jmp        # jmp | working | published | wip
date: 2025-11-01
coauthors:
  - { name: "Coauthor One", url: "https://..." }
  - { name: "Coauthor Two" }
paperurl: "/files/paper.pdf"
slidesurl: "/files/slides.pdf"
venue: "Journal Name, Vol. XX, No. X, 2024"   # for published
doi: "https://doi.org/..."                     # for published
status: "Revise & Resubmit, *Journal Name*"   # optional
---
The body of the file = the paper's abstract. Markdown supported.
```

**Talk**
```yaml
---
title: "Talk Title"
type: "Conference"           # Conference | Seminar | Invited
venue: "NBER Summer Institute"
location: "Cambridge MA"     # optional
date: 2026-07-15
---
```

**Teaching**
```yaml
---
title: "Course Name"
level: "Undergraduate"       # Undergraduate | Graduate
role: "Instructor"           # Instructor | TA
university: "University Name"   # for Instructor
professor: "Prof. Name"         # for TA
term: "Spring 2026"
date: 2026-01-15
---
```

## Local preview (optional)

GitHub Pages will build the site for you on every push. If you want to preview locally:

```bash
bundle install            # first time only
bundle exec jekyll serve  # http://localhost:4000
```

Requires Ruby ≥ 2.6. If your system Ruby is too old, install a current Ruby (`brew install ruby`) and add it to your PATH.

## Deploying

1. Create a repo on GitHub named `<your-username>.github.io`.
2. Push this folder to that repo's `main` branch.
3. In repo Settings → Pages, set Source to "Deploy from a branch" → `main` → `/ (root)`.
4. Live in ~30 seconds at `https://<your-username>.github.io`.

## File map

```
_config.yml          site-wide settings
_data/news.yml       homepage news items
_layouts/            default layout (head, header, nav, footer)
_includes/           small partials: nav.html, publication.html, talk.html, course.html
_publications/       one .md per paper
_talks/              one .md per talk
_teaching/           one .md per course
index.html           about page
publications.html    publications listing
talks.html           talks listing
teaching.html        teaching listing
cv.html              CV page
styles.css           styling (rarely edited)
files/               PDFs (CV, papers, slides)
images/              profile photo, etc.
```
