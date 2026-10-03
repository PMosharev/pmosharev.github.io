# Pavel Mosharev — personal website v0.1

A single English homepage for GitHub Pages, written in semantic HTML and CSS.
There is no build step, framework, analytics, or external asset dependency.
The only JavaScript is a small inline handler for the Email action.

## Files

- `index.html` — public biography, affiliation, research interests, contact and profile links.
- `content/about.md` — editable autobiography text for the About section.
- `styles.css` — responsive layout and a light Orbital Minimalism palette.
- `assets/DSC06850.jpg` — outdoor homepage portrait, with embedded personal metadata removed.
- `assets/portrait.jpg` — retained professional portrait, with embedded metadata removed.
- `assets/favicon.svg` — primary orbital favicon.
- `assets/favicon-32.png` — 32px PNG favicon fallback, rendered from the SVG.
- `assets/apple-touch-icon.png` — 180px touch icon using the same SVG on an opaque navy background.
- `assets/social-preview.jpg` — 1200 × 630 sharing image using the current outdoor portrait.
- `files/Pavel_Mosharev_CV_EN.pdf` — current public English CV.
- `files/Pavel_Mosharev_CV_ZH.pdf` — current frozen public Chinese CV.
- `.nojekyll` — serve the static files without Jekyll processing.

## Preview

Open `index.html` in a browser. Relative links also work directly from the filesystem;
no server or package installation is needed. Check both a wide window and a narrow
mobile-sized window, and open both CV links before publishing. The Email button
requires JavaScript and supports mouse and native keyboard activation. Its click
handler assembles the address from separate pieces and opens a normal `mailto:`
link. This discourages trivial static scraping; it is not strong bot protection,
and the public CVs still contain the public email. With JavaScript disabled, the
button has no effect.

For GitHub Pages, select **Deploy from a branch** in the repository's Pages settings
and choose the publishing branch and **/ (root)** folder.

## Content and asset provenance

Reviewed on 2 October 2026. The authoritative career repository remains separate
and read-only for this website work:

- Editorial reference: `career_profile/cv/public_en.md`.
- PDF source: `career_profile/output/public_en/public_en.pdf`, copied unchanged.
- Chinese PDF source: `career_profile/output/public_cn/public_cn.pdf`, copied
  unchanged from the current frozen public export on 3 October 2026.
- Homepage photo: the outdoor `assets/DSC06850.jpg` supplied in this website
  repository. EXIF/XMP, Photoshop/IPTC, and Ducky metadata segments were removed
  without re-encoding; compressed image data and the Adobe color-transform marker
  were preserved. A broad square CSS crop keeps the outdoor setting and upper
  body inside the existing circular frame and orbital arc.
- Retained professional photo source: `career_profile/assets/photos/pavel_mosharev_cn.jpg`, identified as
  an approved portrait by its accompanying README. The local copy retains the
  original JPEG image data; EXIF/XMP, comment, and editorial metadata segments
  were removed for public distribution.
- The four profile URLs match the public CV and the verified records in
  `career_profile/data/profiles.yaml`.

The homepage's professional facts and public email follow the public CV;
the autobiographical About section follows `content/about.md`.
The completed visiting appointment is not presented as a current affiliation.
No canonical data files, private contacts, build intermediates, or source archives
are included here. The PDF's public content and metadata and the portrait's
metadata were reviewed before copying.

The visual reference is `Style_guide/Orbital_minimalism/STYLE.md` (v1.1, from the
latest v8 reference bundle). The site inherits the Lunar palette: Ice White,
Void Black, Midnight Navy, Orbital Blue, Halo Blue, and Lunar Gray. Arial/Helvetica
use the guide's system-font fallback. Generous spacing, left alignment, restrained
hierarchy, and one original inline SVG arc adapt the identity to a webpage.
No design-system images, PDFs, fonts, or archives are copied.

## v0.1 validation

Basic HTML nesting/entity and CSS checks, local asset paths, public-CV URL matches,
PDF byte comparison, photo image-data comparison, and `git diff --check` passed.
Text contrast is at least 6.54:1. Installed Chrome was used to inspect desktop
rendering and fixed 320px and 390px mobile viewports; both mobile checks reported
no horizontal overflow. Browser fixtures and screenshots are outside this repository.
GitHub, Google Scholar, and ORCID returned HTTP 200. LinkedIn returned HTTP 999
to the automated request; its URL matches the public CV but should be opened manually.
No Python environment, packages, or build tooling were used.

## Favicon and sharing assets

Added on 3 October 2026 using the existing Orbital Minimalism v1.1 guide and
homepage palette. The favicon uses Midnight Navy `#161D32`, an Ice White
`#EDEEF0` open orbital arc, and one Halo Blue `#6A7CAC` node. The sharing image
also uses Void Black `#02040B` for the name and Orbital Blue `#465377` for the
specialization. No design-system source assets or fonts were copied.

The preview was composed locally in installed Chrome using an sRGB canvas,
Arial text, the existing `assets/DSC06850.jpg`, and one subtle Halo Blue arc.
The 360px square portrait uses the homepage's 50%/60% positioning and 1.15 zoom:
source crop `(166.30435, 206.50435, 2217.39130, 2217.39130)` from the 2550 × 2617
photo. It is placed at `(756, 135)` with 16px rounded corners. The name, role,
and specialization use 56px semibold, 28px regular, and 24px regular Arial.
The JPEG uses encoder quality 0.88 and occupies 53,656 bytes (52.4 KiB).
Unnecessary APP metadata was removed without changing compressed image data;
only the minimal JFIF header remains. Both PNGs contain only image chunks.

The head declares the canonical homepage URL, SVG and PNG favicon links, the
touch icon, Open Graph website fields, and a Twitter/X large-image card.
Image dimensions/type and descriptive image alt text are included. Sharing URLs
are absolute. No X account fields are declared. The existing meta description,
page body, and stylesheet remain unchanged.

Validation used installed Windows Chrome and Node.js v18.19.1, without Python,
package installation, or downloads. Commands included
`bash /tmp/orbital-sharing-validation/render.sh`,
`bash /tmp/orbital-sharing-validation/validate-browser.sh`,
`node /tmp/orbital-sharing-validation/strip-jpeg-metadata.cjs`,
`node /tmp/orbital-sharing-validation/check.cjs`, and `git diff --check`.
Temporary fixtures and screenshots live outside the repository. Checks cover
browser asset loading, 16/32px rendering, exact metadata, local paths, HTML
nesting and IDs, unchanged body/description, image dimensions, and PNG/JPEG
metadata. The social image was visually inspected at 1200 × 630 and 600 × 315.
The isolated non-headless Chrome check produced no inspectable window, so actual
visible-tab display remains unverified; headless browser loading and small-size
icon rendering passed.

## Updating

Edit the text and links directly in `index.html`, and adjust appearance in
`styles.css`. The editable autobiography text lives in `content/about.md`; when
it changes, update the About section in `index.html` to match. There is deliberately
no Markdown build system yet. Keep facts aligned with the current public English
CV. Replace the PDFs at the same local filenames when new public exports are
available. Use only an approved portrait and remove embedded personal metadata
from future photo copies.
Review the page and PDF for private information, check every link, and test a narrow
window after updates. Keep v0.1 as a small static page.
