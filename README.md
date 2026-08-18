# Portfolio — aazainumrani.github.io

Single-page portfolio site. One HTML file, no build step, no dependencies.

## Put it live

**Option A — root domain (recommended).** Create a public repo named exactly
`AazainUmrani.github.io`, push `index.html` and `Aazain_Umrani_CV.pdf` to the
`main` branch, and it goes live at **https://aazainumrani.github.io** within a
minute or two. Nothing to configure.

```bash
git init
git add .
git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/AazainUmrani/AazainUmrani.github.io.git
git push -u origin main
```

**Option B — project repo.** Push to any repo (e.g. `portfolio`), then
Settings → Pages → Source: *Deploy from a branch* → `main` / `/ (root)` → Save.
Live at `https://aazainumrani.github.io/portfolio/`.

## Before you push — three things to fill in

1. **Project links.** Every project title currently points at your GitHub
   profile. Search the file for `TODO: replace href with the repo URL` and swap
   in the real repos. If a project has no public repo, delete the `<a>` wrapper
   and leave the plain title.
2. **The CV.** `Aazain_Umrani_CV.pdf` sits next to `index.html` and the
   "Read the CV" button links to it. Replace the file whenever you update it,
   keeping the filename, and the link keeps working.
3. **Phone number.** Deliberately left off — a public page gets scraped.
   Email and LinkedIn are the contact routes.

## Editing

Everything is in `index.html`: content in the body, design tokens (colours,
fonts, spacing) in the `:root` block at the top of the `<style>` tag.

- Add a project: copy one `<article class="work">` block and edit it. Keep the
  four `<span class="brk">` elements — they draw the corner brackets on hover.
- The first card uses `work--lead` for the full-width two-column treatment.
  Move that class to whichever project you want to headline.
- Metrics are optional. Drop the whole `<dl class="metrics">` block if a
  project has no numbers worth quoting — better than padding it with vague ones.

## Notes

Type is Archivo / Source Serif 4 / IBM Plex Mono, loaded from Google Fonts;
fallbacks are set so the page still holds up if that request is blocked.
Responsive to 360px, keyboard-focusable, and `prefers-reduced-motion` is
respected.
