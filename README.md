# Dr. Kanchan Chaudhary — Jekyll / GitHub Pages Portfolio (Option 3)

Markdown-first academic portfolio for GitHub Pages’ native Jekyll support.
Content matches the static site in `../kanchan-portfolio/` (resume May 2026 + Kauvery visiting cards).

| File | Purpose |
|---|---|
| `index.md` | All clinical / academic content + YAML front matter |
| `_config.yml` | Site title, theme (`minima`), SEO, plugins |
| `Gemfile` | Local preview via `github-pages` gem |
| `README.md` | This guide |

---

## What’s in `index.md`

1. Executive Summary & Clinical Background  
2. Qualifications, Fellowships & Board Certifications  
3. Clinical & Surgical Expertise  
4. Select Peer-Reviewed Publications & Book Chapters  
5. Professional Affiliations (AOI, Indian Society of Otology, NEBAOI)  
6. Clinic Schedule & Contact Information  

Front matter uses fields that work with **minima** (GitHub’s default theme) and transfer cleanly to **AcademicPages** if you later fork that theme.

---

## Configure `_config.yml` (before first publish)

Edit these three lines:

```yaml
url: "https://YOUR-USERNAME.github.io"
# If the repo is a project site (not USERNAME.github.io):
# baseurl: "/ent-surgeon-portfolio"
```

Also replace social placeholders in `index.md` (LinkedIn / ResearchGate / Doximity) when you have URLs.

### Theme choices

| Theme | How |
|---|---|
| **minima** (default) | Already set: `theme: minima`. Zero setup on GitHub Pages. |
| **AcademicPages** | Fork [academicpages/academicpages.github.io](https://github.com/academicpages/academicpages.github.io), rename the repo, then paste the section bodies from this `index.md` into `_pages/about.md` / publications YAML as needed. Keep their `_config.yml` and merge author fields. |

---

## Preview locally (optional)

Needs Ruby 3.x.

```bash
cd kanchan-portfolio-jekyll
bundle install
bundle exec jekyll serve
```

Open <http://127.0.0.1:4000>. Stop with `Ctrl+C`.

---

## Step-by-step: host on github.io

### 1. Create a GitHub repository

1. Log in at <https://github.com>.  
2. **New repository**.  
3. Name it one of:
   - **`YOUR-USERNAME.github.io`** — site at `https://YOUR-USERNAME.github.io`  
   - **`ent-surgeon-portfolio`** (or similar) — site at `https://YOUR-USERNAME.github.io/ent-surgeon-portfolio` (set `baseurl` in `_config.yml`)  
4. Set visibility to **Public**.  
5. Do **not** add a README if you will push this folder as-is (avoids merge noise). Create the empty repo.

### 2. Upload the code

**Option A — drag and drop**

1. Open the empty repo on GitHub.  
2. Upload `index.md`, `_config.yml`, and `Gemfile` (README optional).  
3. Commit to the `main` branch.

**Option B — git from this folder**

```bash
cd kanchan-portfolio-jekyll
git init
git add index.md _config.yml Gemfile README.md
git commit -m "Add Jekyll ENT portfolio for GitHub Pages"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-USERNAME.github.io.git
git push -u origin main
```

> Do **not** add a `.nojekyll` file here — you *want* Jekyll to build Markdown into HTML.

### 3. Enable GitHub Pages

1. Repo → **Settings** → **Pages**.  
2. Under **Build and deployment** → **Source**, choose **Deploy from a branch**.  
3. Branch: **`main`**, folder: **`/` (root)** → **Save**.  
4. Wait 1–2 minutes. The Pages panel will show the live URL.

GitHub runs Jekyll automatically: `index.md` → HTML via the `minima` theme.

### 4. Access the site

- User site: `https://YOUR-USERNAME.github.io`  
- Project site: `https://YOUR-USERNAME.github.io/REPO-NAME`  

Hard-refresh (`Cmd+Shift+R`) if an old page is cached.

---

## Editing content later

| Change | File |
|---|---|
| Bio, pubs, clinics | `index.md` |
| Site title, URL, email | `_config.yml` |
| Theme / nav | `_config.yml` (`theme`, `header_pages`) |

Commit and push; Pages rebuilds in about a minute.

---

## Relationship to the HTML portfolio

| | `kanchan-portfolio/` | `kanchan-portfolio-jekyll/` (this) |
|---|---|---|
| Stack | Static HTML / CSS / JS | Markdown + Jekyll |
| Look | Custom Kauvery-matched design | Theme-driven (minima / AcademicPages) |
| Best for | Patient-facing branded site | Academic CV / quick GH Pages publish |
| Deploy | Needs `.nojekyll` | Native Jekyll build |

Keep the HTML site as the primary patient site; use this Jekyll package if you want a content-first academic page with almost no frontend code.

---

## Open questions (same as HTML site)

- Exact Kauvery joining month  
- Which campus she primarily sits at + OPD timings  
- Live LinkedIn / ResearchGate / Doximity URLs  
