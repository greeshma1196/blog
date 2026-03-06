# Iteration 1 - 06-03-26

## Goal
Revive the blog UI with a Bold & Colorful visual identity.

## What Was Done

### Setup
- Created `work_log/` folder for tracking iterations
- Updated `CLAUDE.md` with work log conventions

### Phase 1: Fix Homepage & Enable Excerpts
- Updated `_config.yml`: added `title`, `description`, `show_excerpts: true`, set `minima.skin: auto`
- Replaced blank `index.md` with hybrid homepage (intro section + post list)
- Added `tags` front matter to both blog posts

### Phase 2: Bold & Colorful Styling
- `_sass/minima/custom-variables.scss`: overrode all Minima color variables with Bold palette (cream bg, coral/teal accents, charcoal dark mode)
- `_sass/minima/custom-styles.scss`: added styles for intro section (gradient bg, colored border), post cards (colored left borders, hover lift), tag pills (vibrant colors), reading time, dark mode toggle button, mobile responsive adjustments
- Added Google Font (Space Grotesk) via `_includes/custom-head.html`

### Phase 3: Dark Mode Toggle
- Added `[data-theme="dark"]` and `[data-theme="light"]` CSS custom property overrides
- Added flash-prevention inline script in `<head>` (reads localStorage before paint)
- Added sun/moon toggle button in header navigation (`_includes/header.html`)
- Added toggle JS in `_layouts/base.html` (persists choice to localStorage)

### Phase 4: Reading Time & Tags
- `_layouts/home.html`: post cards now show reading time and tag badges
- `_layouts/post.html`: reading time and tags displayed in post header

### Phase 5: Favicon & Branding
- Created SVG favicon (`assets/favicon.svg`) with coral "G" on rounded rectangle
- Linked favicon in `_includes/custom-head.html`

## Files Modified
- `_config.yml`
- `index.md`
- `_layouts/home.html`
- `_layouts/post.html`
- `_layouts/base.html`
- `_includes/header.html`
- `_includes/custom-head.html`
- `_sass/minima/custom-variables.scss`
- `_sass/minima/custom-styles.scss`
- `_posts/2022-11-11-how-does-the-internet-work.md`
- `_posts/2024-01-15-cli-task-manager.md`

### Fixes & Tooling
- Excluded `CLAUDE.md` and `work_log/` from Jekyll build via `_config.yml`
- Created `Makefile` with `install`, `serve` (with `--livereload`), `build`, and `clean` targets
- Added "close iteration" rule to `CLAUDE.md` (review session, update iteration doc, draft commit message)

## Files Modified
- `_config.yml`
- `index.md`
- `_layouts/home.html`
- `_layouts/post.html`
- `_layouts/base.html`
- `_includes/header.html`
- `_includes/custom-head.html`
- `_sass/minima/custom-variables.scss`
- `_sass/minima/custom-styles.scss`
- `_posts/2022-11-11-how-does-the-internet-work.md`
- `_posts/2024-01-15-cli-task-manager.md`
- `CLAUDE.md`

## Files Created
- `work_log/06-03-26-iteration-1.md`
- `assets/favicon.svg`
- `Makefile`

## Next Steps
- Run `bundle install` then `bundle exec jekyll serve` to verify locally
- Fine-tune colors/spacing after visual review
- Consider adding tag archive page
- Update resume and about page content
