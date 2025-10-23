# Repository Guidelines

## Project Structure & Module Organization
OakLife is a static marketing site for the AceCoach iOS app. Core entry points sit in the repo root: `index.html` (landing page), `privacy.html` (policy), and `tennis.html` (alternate design concept). Shared imagery lives beside them, e.g., `tennis_background.png`. Keep new assets lightweight, compress them before committing, and group any future experiments in clearly named HTML files at the root unless we introduce a bundler.

## Build, Test, and Development Commands
- `open index.html` — quickest way to preview changes in your default browser.
- `python3 -m http.server 8000` — serves the root locally so you can confirm relative paths and caching. Visit http://localhost:8000 after running.
- `npx htmlhint *.html` — optional lint pass to catch malformed markup; install Node 18+ locally if you plan to run it.

## Coding Style & Naming Conventions
Use four-space indentation and keep CSS within the existing `<style>` blocks until we adopt an external stylesheet. Favor semantic HTML5 elements (`header`, `section`, `footer`) and compact class names in lower-case with hyphens. Reuse the current color palette and emoji treatments for brand consistency. When adding JavaScript, wrap code in a single `<script>` tag near the end of the document to avoid blocking rendering.

## Testing Guidelines
Manually verify each page in Safari and Chrome, checking both desktop and iPhone/iPad responsive breakpoints (≤768px). Confirm hero sections, gradients, and app-store callouts render cleanly against the background imagery. Re-run `npx htmlhint` or an online W3C validator after structural edits. Capture before/after screenshots if the visual layout changes.

## Commit & Pull Request Guidelines
Keep commits small, written in the imperative mood ("Add responsive hero"), and optionally scoped with prefixes like `feat:` or `fix:` as seen in recent history. Reference any related issue or tracking doc in the body. Pull requests should explain the intent, list affected pages, embed key screenshots or GIFs, and note manual test coverage so reviewers can reproduce your checks quickly.
