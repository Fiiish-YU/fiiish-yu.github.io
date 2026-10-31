# Project Guidelines

## Project structure

- This is a Jekyll site using the Minima theme with custom layouts and Sass.
- Top-level folders such as `life/`, `games/`, `notebook/`, `paintings/`, and `photography/` contain section landing pages.
- `_includes/`, `_layouts/`, and `_sass/` contain shared site components and styles. Keep navigation changes consistent with the section pages.
- Photography entries are stored in `_photography/`; their publishing guide is in [docs/photography.md](docs/photography.md).

## Conventions

- Follow the existing Jekyll Liquid, YAML front matter, HTML, and Sass patterns.
- Keep visitor-facing text consistent with the site's Chinese content and existing visual style.
- Avoid adding dependencies or changing unrelated sections for a focused feature.
- Keep section-specific authoring instructions in separate documents under `docs/`, not in the project README.

## Git commits

- After completing a user-requested fix, change, or addition, create a Git commit containing only the changes for that task.
- Use a conventional type prefix that matches the change, such as `fix:`, `feat:`, `refactor:`, `docs:`, `test:`, or `chore:`.
- Do not include unrelated pre-existing working-tree changes in the commit.

## Validation

- Run `git diff --check` after edits.
- If Jekyll is available, build the site with `jekyll build` and address build errors caused by the change.
