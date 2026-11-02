# Academic homepage handoff

## Repository and publication

- Repository: https://github.com/houhi/houhi.github.io ; default branch: `master`.
- Public URL: https://houhi.github.io/ .
- The initial personalized homepage was published through PR #1 and merge commit `de92333d21bdae565a704927419e8ddf1abd9191`. Its Pages workflow `41479786666` completed successfully, and the public homepage was verified to contain Pengfei Zhang’s new content.
- The original `homepage/` directory is an independent source checkpoint. The sibling `../homepage-publication/` is the remote-history-preserving clone; perform future commits, branches, and pushes there. Never force-push the checkpoint root commit.
- The authorship/mentor/logo refinements were published through PR #2, merge commit `c39d8d59b582a3b04a76eb50472766196f63fbd4`. The follow-up branch `codex/add-ramr-framework` adds the last original framework figure after the user opened the PDF.
- Official GitHub CLI browser login for `houhi` is active, using the macOS keyring. CLI: `/Users/rocwelzhang/.cache/codex-tools/v2.103.3/gh`. The ChatGPT GitHub connector previously denied writes; use authenticated Git/CLI for publication.
- Pages builds the repository root on `master` using the existing native Pages workflow. Keep new source changes on a branch, build locally, then publish through a PR and verify the resulting deployment and URL.

## Latest user requirements (2026-11-03)

- RAMR: the user identifies as a co-first author and requests Pengfei Zhang first in the displayed author list. `display_authors` implements the presentation order and the co-first-author marker. `authors` and BibTeX preserve the formal publication metadata. The original PDF confirms that the first five published authors contributed equally; all five have contribution markers in `display_authors`.
- Do not display under-review manuscripts anywhere on the public website or CV. The structured data is retained under `_data/manuscripts.yml` but is not rendered.
- Include industry mentor names and links in the biography and experience/CV: Tencent mentor Xingxuan Zhou (周星玄), Scholar `aKJaW7cAAAAJ`; JD mentor Yanyan Zou, Scholar `pkY_HogAAAAJ`. Both names were verified from the user-provided Scholar profiles.
- Show official UESTC, Beijing Forestry University, Tencent, and JD logos in education/experience and CV.
- Show actual framework figures for all three published papers. CARD and EyeCRS use author-provided figures. RAMaR uses Figure 1 from page 2 of the published PDF, downloaded through Chrome after the user completed the ACM access check. All three figures have full-size image links. Never substitute invented framework diagrams.

## Content and assets

- `_data/profile.yml`: biography, education, experience, named mentors, awards, and contacts.
- `_publications/`: three published papers; Pengfei Zhang is bolded.
- `assets/images/profile.jpg`: portrait from the supplied CV. Never copy the original resume PDF or its phone number into the public site.
- `cv.html`: printable public CV generated from shared structured data.
- `assets/vendor/bootstrap.min.css`: required locally vendored asset; keep tracked. `.gitignore` ignores only root-level `/vendor/` installs.
- `ASSET_SOURCES.md`: source URLs for logos and framework images; excluded from generated web output.
- Retain the template's MIT license and attribution to luost26/academic-homepage.

## Build and validation

- System Ruby 2.6 is too old for current dependencies. Standalone Ruby 3.4.5: `/Users/rocwelzhang/.cache/codex-tools/ruby/portable-ruby/3.4.5/bin/`. Prepend to PATH for Bundler commands.
- Dependencies are installed in the publication clone under ignored `vendor/bundle/`; GitHub Pages 232 / Jekyll 3.10.0 and Bundler 2.6.9 are locked for local builds.
- Run `bundle exec jekyll build --trace` after source changes. The initial and refined local builds passed.
- Initial browser QA covered home/publications/CV navigation, desktop and 390px mobile widths, portrait loading, and console errors. Repeat focused checks for changed content and images.
- All four generated HTML pages must retain valid internal links/assets/fragments, one h1, descriptive image alt text, and no unresolved Liquid. Confirm under-review titles are absent from generated output.
- All original framework image sources are now resolved. Continue ordinary GitHub publication without asking the user to reconfirm authorized changes. Verify the latest workflow and the live home/publications/CV pages before reporting completion.
