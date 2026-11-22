# Romina F. Murga — Academic Portfolio & Web CV

Personal academic website and printable CV of **Romina Francisca Murga Moraga** — Ph.D. Candidate in Engineering Systems at the University of Talca, researching polymeric and biodegradable nanoparticles for mineral processing and froth flotation.

Built with [Jekyll](https://jekyllrb.com/) and the [AcademicPages](https://github.com/academicpages/academicpages.github.io) theme.

## Structure & Customization

- **Site & Author Profile**: [`_config.yml`](_config.yml) — Configure site title, base URL, biography, email, ORCID, LinkedIn, and other academic profiles.
- **Profile Photo**: Replace `images/profile.svg` (or upload `images/profile.jpg` and update `author.avatar` in `_config.yml`) with a personal portrait photo.
- **Home / About Page**: [`_pages/about.md`](_pages/about.md) — Research thrusts, milestones, and selected journal articles.
- **Curriculum Vitae & Printable PDF Export**:
  - Web CV: [`_pages/cv.md`](_pages/cv.md)
  - LaTeX-styled PDF Export (`/cv-export/`): [`_pages/cv-export.html`](_pages/cv-export.html)
  - Modular CV sections in `_includes/`: `education.md`, `skills.md`, `research_projects.md`, `research_stays.md`, `teaching_cv.md`, `students.md`, `service_outreach.md`, `work_experience.md`, `technical_skills.md`, and `collaborators.md`.
- **Publications & ORCID Synchronization**:
  - Master BibTeX file: [`files/RMurga.bib`](files/RMurga.bib)
  - Regenerate `_publications/*.md` and `_data/cv.json` locally:
    ```bash
    python3 scripts/sync_orcid_publications.py --bib-only
    ```
  - Fetch new works from ORCID (`0009-0007-8573-9996`) and regenerate:
    ```bash
    python3 scripts/sync_orcid_publications.py
    ```
- **Teaching & Collaborators**: [`_pages/teaching.html`](_pages/teaching.html) and [`_pages/people.md`](_pages/people.md).

## Running Locally

```bash
bundle config set --local path 'vendor/bundle'
bundle install
bundle exec jekyll serve -l -H localhost
```

Or via Docker:

```bash
docker compose up
```
