# Repository guidance

This is a small personal website served as static files on GitHub Pages.
Read [docs/maintenance.md](docs/maintenance.md) before making changes.

## Editing

- Keep the site as plain HTML and CSS with the existing small inline email handler.
  Preserve the established design and avoid adding frameworks, build tooling,
  analytics, or external asset dependencies unless requested.
- Keep changes within the requested scope. Documentation-only work must leave
  site files, content, assets, and PDFs unchanged.
- Use the approved public English CV for professional facts and profile links.
  Keep `content/about.md` and the About section in `index.html` synchronized when
  editing the autobiography; Markdown is not rendered automatically.
- The separate `career_profile` repository is an editorial reference and must
  remain read-only during website work. Do not invent biographical claims or
  publish private source material. Use approved public PDF exports and photos;
  review embedded metadata before adding or replacing assets.
- Keep the README concise and public-facing. Put maintenance details in `docs/`.

## Verification

- Run `git diff --check` and review the changed-file list.
- For site changes, open `index.html` in a browser and follow the maintenance
  guide's checks for layout, keyboard access, links, PDFs, and sharing assets.
- For documentation-only changes, check relative documentation links and confirm
  existing non-documentation files are unchanged. Browser testing is unnecessary
  when the site files are unchanged.
- Report what was checked and any limitations. Treat historical validation notes
  as past results, not evidence of a new check.
