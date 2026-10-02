# Pavel Mosharev — personal website v0.1

A single English homepage for GitHub Pages, written in semantic HTML and CSS.
There is no build step, JavaScript, framework, analytics, or external asset dependency.

## Files

- `index.html` — public biography, affiliation, research interests, contact and profile links.
- `styles.css` — responsive layout and a light Orbital Minimalism palette.
- `assets/portrait.jpg` — approved professional portrait, with embedded metadata removed.
- `files/Pavel_Mosharev_CV_EN.pdf` — current public English CV.
- `.nojekyll` — serve the static files without Jekyll processing.

## Preview

Open `index.html` in a browser. Relative links also work directly from the filesystem;
no server or package installation is needed. Check both a wide window and a narrow
mobile-sized window, and open the CV link before publishing.

For GitHub Pages, select **Deploy from a branch** in the repository's Pages settings
and choose the publishing branch and **/ (root)** folder.

## Content and asset provenance

Reviewed on 2 October 2026. The authoritative career repository remains separate
and read-only for this website work:

- Editorial reference: `career_profile/cv/public_en.md`.
- PDF source: `career_profile/output/public_en/public_en.pdf`, copied unchanged.
- Photo source: `career_profile/assets/photos/pavel_mosharev_cn.jpg`, identified as
  an approved portrait by its accompanying README. The local copy retains the
  original JPEG image data; EXIF/XMP, comment, and editorial metadata segments
  were removed for public distribution.
- The four profile URLs match the public CV and the verified records in
  `career_profile/data/profiles.yaml`.

The homepage uses only the public CV's professional facts and public email.
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

## Updating

Edit the text and links directly in `index.html`, and adjust appearance in
`styles.css`. Keep facts aligned with the current public English CV. Replace the
PDF at the same local filename when a new public export is available. Use only an
approved portrait and remove embedded personal metadata from future photo copies.
Review the page and PDF for private information, check every link, and test a narrow
window after updates. Keep v0.1 as a small static page.
