# Agent notes

This repository is a written guide (not an app): the PARA method / a second brain in the iPhone and iPad **Notes** app on **iOS 27** and **iPadOS 27** (minimum for readers). Human readers matter more than tooling polish; keep edits small and in voice with the existing pages.

## Repository layout

- **`docs/`** - Jekyll site (Minima, GFM). Published via GitHub Pages from `main` → `/docs`. See `docs/_config.yml` for `baseurl` (`/ios-notes-para`) and hosting notes. Do not add a custom domain on this repo (it would clash with the profile site).
- **`README.md`** - Entry point on GitHub; its numbered guide list should stay aligned with `docs/index.md` when you change navigation or titles.
- **`docs/images/`** - SVG diagrams referenced from the markdown.
- **`book/`** - Export-only metadata and front matter for PDF/EPUB builds (`scripts/build-book.sh`). Not published on the site. Keep [`book/chapters.txt`](book/chapters.txt) in the same order as the numbered list in [`docs/index.md`](docs/index.md). CI enforces that order and README ↔ index navigation via `scripts/check-guide.py`.

## Language and punctuation

- **UK English** in all reader-facing prose: *recognise*, *behaviour*, *colour*, *organise* (including setup tables), and similar. Keep US spellings only where they are the official product name (e.g. Notes **Smart Folder**).
- **No em dashes** (`—`). Use a spaced hyphen instead: ` - ` (e.g. `**Notes** - the built-in inbox…`, `[setup](setup.md) - the tap-by-tap afternoon`).
- **Quotation marks** for example note titles and short quoted phrases: use curly quotes `“` and `”` as in the existing docs, not straight `"`.

## Voice and content

- Address the reader as **you**. Calm, practical, slightly opinionated; avoid hype and filler.
- **iPhone-first.** Mac and web are mentioned only where behaviour differs (`docs/limits.md` is the honest edge cases page).
- **PARA attribution:** Tiago Forte’s PARA method and Building a Second Brain are the foundation; this is an independent guide, not an Apple or Forte Labs product.
- **Naming:** Folder names in bold (**Notes**, **Projects**, **Areas**, **Resources**, **Archives**). Overlay tags in backticks with the hash (`#work`, `#personal`). Smart Folder names match the guide tables when used.
- **Scope:** The main path is four folders plus the built-in Notes folder as Inbox. Tags, Smart Folders, and Apple Intelligence extras live in `docs/advanced.md`. Do not expand the core taxonomy without a deliberate editorial reason. Next actions belong in Reminders, not in Notes.

## Editorial review (agents)

- **Diff / PR-style:** `/review-changes` if the command exists in this workspace
- **Full publication audit:** keep the same bar as the sibling Reminders GTD guide: UK English, spaced hyphens, device honesty

## Issues and pull requests

- Human workflow and checklists: [CONTRIBUTING.md](CONTRIBUTING.md) and [.github/pull_request_template.md](.github/pull_request_template.md).
- Label names and meanings: [.github/labels.yml](.github/labels.yml). Apply one change-type label and an `area:*` label when the edit is localised; use `needs-device-check` for setup and Notes UI changes.
- Do not open issues or pull requests unless the user asks.

## When editing

- Match the tone and structure of neighbouring sections before adding new ones.
- Prefer updating diagrams in `docs/images/` when the model changes, not only the text.
- Do not commit unless the user asks. Do not put secrets in the repo.
