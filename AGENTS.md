# AGENTS.md — Personal

> Compact instruction file for OpenCode sessions in this repo.

## Repo overview

- **Type**: Personal portfolio — Jekyll static site for GitHub Pages.
- **Stack**: Jekyll (GitHub Pages native), CSS custom properties, no JS.
- **Engram project key**: `personal`
- **No build step required locally** — GitHub Pages compiles Jekyll on push.
- **Local serve** (optional): `bundle exec jekyll serve` if Ruby + Bundler installed.

## Structure

- `index.md` — single-page content (hero, projects, about, contact).
- `_layouts/default.html` — minimal HTML shell.
- `_data/projects_en.yml` / `_data/projects_es.yml` — project data per language.
- `_data/i18n/en.yml` / `_data/i18n/es.yml` — UI strings per language.
- `assets/css/main.scss` — styles (SCSS compiled by Jekyll).
- `_config.yml` — site metadata and Jekyll settings.

## i18n Rules (MANDATORY)

This portfolio is bilingual (EN/ES). When editing content:

1. **Check both languages** — if you change a string in one language, check if the equivalent exists in the other.
2. **Simple changes** (rewording, typo fixes, short additions) → apply to both languages automatically.
3. **Complex changes** (restructuring, new sections, tone shifts) → ask the user before modifying the other language.
4. **Never leave one language outdated** — both must stay in sync semantically, even if the wording differs.

## SDD / OpenCode

- Skill registry at `.atl/skill-registry.md` — auto-generated index of installed OpenCode skills.
- Skills live under `~/.config/opencode/skills/`. The registry is a delegator-only index; `SKILL.md` files remain the source of truth.
