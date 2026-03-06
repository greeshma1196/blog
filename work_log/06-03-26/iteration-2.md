# Iteration 2 - 06-03-26

## Goal
Clean up the repo and fix security vulnerabilities.

## What Was Done

### Repo Cleanup
- Updated `.gitignore` to exclude `_site/`, `.jekyll-cache/`, `.sass-cache/`, `vendor/`
- Removed `_site/` from git tracking (13 files) — build output no longer committed
- Deleted 19 unused social icon SVGs from `_includes/social-icons/` (kept github.svg, linkedin.svg, and rss.svg)
- Restored `rss.svg` after build failure — hardcoded in Minima's `minima-social-icons.liquid`
- Deleted 5 unused skin SCSS files from `_sass/minima/skins/` (kept auto.scss)
- Removed unused `_includes/google-analytics.html` and `_includes/disqus_comments.html`
- Removed disqus include reference from `_layouts/post.html`
- Populated empty `README.md` with project description and setup instructions

### Security Fixes
- Added `| escape` filter to post tags in `_layouts/home.html` and `_layouts/post.html`
- Added `| escape` filter to author names in `_layouts/post.html`
- SRI for Google Fonts skipped — not practical (Google serves different CSS per browser User-Agent)

### CLAUDE.md Updates
- Updated work log convention to use date folders (`work_log/dd-mm-yy/iteration-N.md`)
- Added "plan for next iteration" rule

## Files Modified
- `.gitignore`
- `_layouts/post.html`
- `_layouts/home.html`
- `README.md`
- `CLAUDE.md`

## Files Deleted
- `_site/` (13 tracked files removed from git)
- 19 unused social icon SVGs
- 5 unused skin SCSS files (classic, dark, solarized, solarized-dark, solarized-light)
- `_includes/google-analytics.html`
- `_includes/disqus_comments.html`

## Next Steps
- Consider adding a tag archive page
- Update about page and resume content
