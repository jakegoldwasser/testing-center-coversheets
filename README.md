# Testing Center Coversheets

Fill in one assessment's shared details once, add every student taking it, and print a full stack of individual testing-center coversheets — one page per student, formatted to match Horace Mann's coversheet.

Runs entirely in the browser: no server, no accounts, nothing uploaded. Everything you type about students lives only in that browser tab's memory and is gone when you close or reload the page. Only the teacher's own email and extension are remembered in the browser (`localStorage`), and typing a known teacher's email (see `KNOWN_TEACHER_EXTENSIONS`) fills in their extension. "Print all coversheets" calls the browser's own print dialog, so "Save as PDF" works too without this tool generating a PDF itself.

## Filling in the Test Center's Google Form

"Fill Google Form…" opens a list of the queued students. Each one opens the Test Center's official cover-sheet Google Form in a new tab with that student's answers already filled in, using Google's pre-filled link (`entry.<id>=` query params). You review the form, tick "Record my email", attach the exam and press Submit. The tool never submits anything itself. The form's entry IDs and option wording live in the `GFORM` block in `index.html`; if the Test Center publishes a new form (e.g. for a new school year), re-read them from it.

## Use it

Open `index.html` (works from any static file host, or just double-click it locally) — or use the hosted version via GitHub Pages once enabled for this repo.

## How it's built

Single static HTML file, no build step, no dependencies beyond two Google Fonts. All logic is inline `<script>`/`<style>` in `index.html` — there's no separate, hidden build; what's in this file is exactly what runs in the browser.
