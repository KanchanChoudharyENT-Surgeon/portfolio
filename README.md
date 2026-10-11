# Dr. Kanchan Chaudhary — Portfolio Website

A static, single-page portfolio for GitHub Pages (free hosting). No build step:
plain HTML, CSS and JS.

## Sources
- Resume: `Kanchan_Chaudhary_Resume.pdf` (last updated May 11, 2026)
- Kauvery Hospital visiting cards (Oct 2026): current role, locations, phone numbers

## Files
| File | Purpose |
|---|---|
| `index.html` | All content |
| `style.css` | Design (plum / coral / cream palette, matching Kauvery branding) |
| `script.js` | Mobile menu, scroll animations, stat counters |
| `favicon.svg` | "KC" browser tab icon |
| `.nojekyll` | Tells GitHub Pages to serve files as-is |

## Deploy to GitHub Pages
1. Create a free account at <https://github.com> (e.g. username `drkanchanchaudhary`).
2. Create a **public** repository named exactly `<username>.github.io`.
3. Upload every file in this folder (drag-and-drop on the repo page, or `git push`).
4. Repo **Settings → Pages → Source: Deploy from a branch → `main` / root** → Save.
5. After 1–2 minutes the site is live at `https://<username>.github.io`.

Using git from this folder:

```bash
git init && git add . && git commit -m "Portfolio site"
git branch -M main
git remote add origin https://github.com/<username>/<username>.github.io.git
git push -u origin main
```

## Easy edits
- **Photo:** hero uses `photo.jpg` (lab-coat portrait). Replace that file to update.
- **LinkedIn:** the resume mentions LinkedIn but the URL wasn't in the PDF; add a link
  in the contact section once known.
- **Kauvery start date:** the timeline shows "Present"; add the month she joined.

## Open questions
- Exact Kauvery joining date and end date of the Sri Aurobindo Assistant Professor role.
- Which Kauvery campus (Electronic City or Marathahalli) she sits at, and OPD timings.
- Board percentages were left out on purpose; they're in the resume if wanted.
