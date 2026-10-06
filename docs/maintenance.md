# Maintenance guide

This repository contains one English homepage, served directly by GitHub Pages.
It uses semantic HTML, responsive CSS, system fonts, and local assets. There is
no build step, framework, package manifest, analytics, or external asset dependency.

## Repository structure

| Path | Purpose |
| --- | --- |
| [`index.html`](../index.html) | Published biography, affiliation, research interests, About section, contacts, and page metadata. |
| [`styles.css`](../styles.css) | Responsive layout and Orbital Minimalism colors. |
| [`content/about.md`](../content/about.md) | Editorial source for the About section; copied into HTML manually. |
| `assets/` | Homepage photo (`DSC06850.jpg`), retained professional portrait (`portrait.jpg`), favicon files, touch icon, and sharing image. |
| `files/` | Public English and Chinese CV PDFs. |
| [`.nojekyll`](../.nojekyll) | Bypasses Jekyll processing for static hosting. |
| [`README.md`](../README.md) | Public introduction and documentation links. |
| [`AGENTS.md`](../AGENTS.md) | Recurring instructions for coding agents. |

The only JavaScript is the inline Email button handler. It assembles the address
from separate pieces and opens a `mailto:` link. The button supports native mouse
and keyboard activation but has no effect with JavaScript disabled. This only
discourages trivial static scraping; the public CVs also contain the public email.

## Preview and updates

Open `index.html` directly in a browser. Relative assets and CV links work from
the filesystem; no server or package installation is needed.

- Edit page text and links in `index.html`, and appearance in `styles.css`.
- When editing the autobiography, update both `content/about.md` and the About
  section in `index.html`. There is no Markdown rendering or synchronization tool.
- Align professional facts, public email, and profile links with the approved
  public English CV. Keep completed appointments distinct from current affiliations.
- Replace CVs with approved public exports at the existing filenames:
  `files/Pavel_Mosharev_CV_EN.pdf` and `files/Pavel_Mosharev_CV_ZH.pdf`.
- Use approved photos and remove embedded personal metadata from future copies.
  Review both visible content and embedded metadata in PDFs and images before
  publishing. Keep private contacts, source archives, and build intermediates out
  of this public repository.
- If changing the portrait or public description, review `assets/social-preview.jpg`
  and the Open Graph and Twitter/X fields in `index.html` for consistency.

Before publishing site changes, inspect a desktop window and narrow viewports
(320px and 390px), check for horizontal overflow, test keyboard focus and Email
activation, open both PDFs, and check contact and profile links. For asset or
metadata changes, check favicon loading and sharing image paths, dimensions, and
descriptions. Run `git diff --check` and review the diff for unintended changes.
There is no committed automated test suite.

The existing publishing instructions use GitHub Pages **Deploy from a branch**,
with the publishing branch and **/ (root)** folder selected. Preview and review
changes locally before publishing through the repository's established workflow.

## Content and asset provenance

The following records were carried over from the original README. Paths under
`career_profile/` and `Style_guide/` refer to separate source material, not files
included in this repository. The career repository remains authoritative and
read-only for website work.

- **Professional content:** reviewed on 2 October 2026 against
  `career_profile/cv/public_en.md`. The four profile URLs followed the public CV
  and `career_profile/data/profiles.yaml`.
- **CVs:** the English PDF was copied unchanged from
  `career_profile/output/public_en/public_en.pdf`. The Chinese PDF was copied
  unchanged on 3 October 2026 from the frozen public export at
  `career_profile/output/public_cn/public_cn.pdf`.
- **Photos:** `assets/DSC06850.jpg` was supplied in this repository.
  `assets/portrait.jpg` came from the approved photo at
  `career_profile/assets/photos/pavel_mosharev_cn.jpg`. Personal and editorial
  metadata was removed without re-encoding the JPEG image data; the outdoor
  photo's Adobe color-transform marker was preserved.
- **Design:** based on `Style_guide/Orbital_minimalism/STYLE.md`, v1.1 from the v8
  reference bundle. The Lunar palette uses Ice White, Void Black, Midnight Navy,
  Orbital Blue, Halo Blue, and Lunar Gray. Typography uses Arial/Helvetica system
  fallbacks; no design-system images, fonts, PDFs, or archives were copied.
- **Favicons and sharing:** added on 3 October 2026. The orbital SVG has a 32px
  PNG fallback and a 180px touch icon on navy. The 1200 × 630 sharing JPEG was
  composed locally in Chrome with Arial, the outdoor portrait, and an orbital arc.
  Its portrait crop follows the homepage's 50%/60% positioning and 1.15 zoom.
  JPEG metadata was reduced to a minimal JFIF header; both PNGs contain only image
  chunks. Sharing URLs are absolute; image dimensions, type, and alt text are
  declared in `index.html`.

## Historical validation

These are recorded results from the initial v0.1 work and the 3 October 2026
favicon/sharing update, not checks rerun for this documentation reorganization.

HTML/CSS, local paths, public-CV URLs, PDF byte comparisons, photo image-data
comparisons, and whitespace checks were reported as passing. Text contrast was
at least 6.54:1; Chrome checks at 320px and 390px reported no horizontal overflow.
GitHub, Google Scholar, and ORCID returned HTTP 200. LinkedIn returned HTTP 999
to the automated request; its URL matched the CV but still needed manual review.

Sharing asset checks used installed Windows Chrome and Node.js v18.19.1, without
Python, dependency installation, or downloads. They covered asset loading,
16/32px icon rendering, HTML metadata, image dimensions, and embedded metadata.
The sharing image was inspected at full and half size. Headless checks passed;
actual visible-tab favicon display remained unverified. Temporary validation
scripts, fixtures, and screenshots were outside the repository and are not a
reproducible test suite here. Detailed original records remain in Git history.
