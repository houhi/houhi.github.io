# Academic homepage handoff

The user chose `luost26/academic-homepage` (template option 3) and supplied their CV, Scholar profile, and three mentor profile links. The personalized English website is implemented in this directory. Continue from this implementation; do not restart template selection or ask the user to re-enter their CV.

## Publication target and current state

- Repository: `https://github.com/houhi/houhi.github.io`
- Existing default branch: `master`.
- Last observed remote head: `705acba0074e705f55da5663dfbfefe67053cf34`.
- Public URL: `https://houhi.github.io/`.
- The remote still contains the previous Academic Pages template. No remote changes were made.
- The ChatGPT GitHub connection successfully reads this repository, but branch creation returned HTTP 403, `Resource not accessible by integration`. Use a supported Codex GitHub write connection.
- This local repository is an independent checkpoint of the new source, not a clone of the existing remote history. Do not force-push this root commit to the existing repository.

## Resumed preparation (2026-11-03)

- The original checkpoint remains in `homepage/`; the history-preserving remote clone is in sibling directory `../homepage-publication/`.
- Publication branch: `codex/publish-academic-homepage-20261103`, based on remote `master` at `705acba0074e705f55da5663dfbfefe67053cf34`. The old tracked template was fully removed before importing the checkpoint.
- A genuine `bundle exec jekyll build --trace` passed with GitHub Pages 232 / Jekyll 3.10.0 and Ruby 3.4.5. The lockfile includes macOS and Linux platforms.
- Browser QA passed for home, publications, and CV navigation; desktop layout and 390px mobile widths were checked, with no horizontal overflow or console errors. All four generated HTML pages passed internal link, asset, fragment, heading, and image-alt checks.
- System Ruby 2.6 cannot resolve current dependencies. A standalone Ruby is available at `/Users/rocwelzhang/.cache/codex-tools/ruby/portable-ruby/3.4.5/bin/`; use it through PATH. Dependencies are installed in the publication clone under ignored `vendor/bundle/`.
- GitHub CLI is available at `/Users/rocwelzhang/.cache/codex-tools/v2.103.3/gh`. The Git push dry run failed before authentication: `fatal: unable to get password from user`. Browser device authorization has been started; check `gh auth status` before publishing.
- Public site still serves the old template. No remote writes have been made during this resumed preparation. Do not report the new site as live until publication succeeds.

## Continue publishing

1. Read the user's latest instructions and check local and remote state.
2. With working GitHub access, fetch or clone the existing remote. Create a publication branch from its current `master`.
3. Replace the previous template's tracked source with this checkpoint's complete source tree while preserving `.git` and remote history. This is a migration, not an overlay: old `_pages/`, sample publications, legacy layouts, and old template workflows must not remain active.
4. Run a real `bundle exec jekyll build` and fix any issues. Then commit, publish the branch, and finish the PR / Pages publication workflow authorized by the user's request. Verify the Pages build and final URL before reporting it live.
5. If access is still read-only, report the precise blocker and retain these files. Do not retry equivalent denied writes or ask for passwords, TOTP secrets, recovery codes, or personal access tokens in chat.

## Source and content

- `_data/profile.yml`: biography, education, experience, mentor URLs, awards, and contact details.
- `_publications/`: three published papers. Formal titles and author order were checked against public publication metadata. Pengfei Zhang is bolded.
- `_data/manuscripts.yml`: three works explicitly marked under review. Keep these separate from published papers.
- `assets/images/profile.jpg`: the user's portrait extracted from the supplied CV.
- `cv.html`: public, printable CV generated from the same structured information. The original resume PDF was not copied into the website.
- `assets/vendor/bootstrap.min.css`: locally vendored, required asset; ensure it stays tracked. `/vendor/` in `.gitignore` refers only to root-level dependency installs.
- Retain the upstream MIT license and template attribution.
- The two industry mentors are linked using the user-provided Scholar URLs, with the label `Industry mentor`; their names have not yet been verified. Do not guess them.

## Verification already completed

YAML and Front Matter parsing; all include targets; strict LiquidJS rendering of home, publications, CV, and 404; internal asset/link existence; one primary heading per rendered page; portrait alt text; bold author names; removal of old sample identities and the resume phone number; self-contained offline preview.

The earlier environment could not run Jekyll, resolve external Git hosts, or bind a preview server. The 2026-11-03 resumed preparation resolved those local limitations and completed the real build and browser QA. GitHub Pages deployment is still unverified.
