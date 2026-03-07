# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Personal blog/portfolio site for Greeshma Mathew, built with Jekyll and hosted on GitHub Pages.

## Commands

- **Install dependencies:** `bundle install`
- **Run locally:** `bundle exec jekyll serve` (serves at http://localhost:4000)
- **Build site:** `bundle exec jekyll build` (output goes to `_site/`)

## Architecture

- **Theme:** Minima (via `github-pages` gem, v232)
- **Config:** `_config.yml` — site author, theme, and social links
- **Posts:** `_posts/` — Markdown files with `YYYY-MM-DD-title.md` naming convention
- **Pages:** Top-level markdown files (`about.markdown`, `resume.markdown`, `index.md`)
- **Layouts:** `_layouts/` — `base.html`, `home.html`, `page.html`, `post.html`
- **Includes:** `_includes/` — partials for header, footer, head, social icons, etc.
- **Styles:** `_sass/minima/` — SCSS files; `custom-styles.scss` and `custom-variables.scss` for overrides
- **Assets:** `docs/assets/images/` for post images; `assets/css/style.scss` as the main stylesheet entry point

## Work Log

- All iteration work is tracked under `work_log/`.
- Iterations are organized in date folders: `work_log/dd-mm-yy/iteration-N.md` (e.g., `work_log/06-03-26/iteration-1.md`).
- Log what was done in each iteration as you go.
- **Closing an iteration:** When the user says "lets close this iteration":
  1. Review the entire session and update the current iteration doc (`work_log/dd-mm-yy/iteration-N.md`) with all changes made.
  2. Create a git commit message summarizing the changes in 50 words or fewer.
- **Planning next iteration:** When the user says "lets plan for next iteration", create a new file under the current date folder: `work_log/dd-mm-yy/iteration-{N+1}.md`.
- **Branching:** Each iteration uses its own git branch named `dd-mm-yy-iteration-N` (e.g., `06-03-26-iteration-1`).

## Notes

- The `_site/` directory is the build output and is committed to the repo (used for GitHub Pages). It should not be edited directly.
- The site uses the `github-pages` gem rather than standalone Jekyll, so available plugins and Jekyll version are constrained by GitHub Pages compatibility.
