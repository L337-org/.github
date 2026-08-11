# Copilot instructions for L337-org/.github

## What this repo is

`.github` is GitHub's special **org-wide community-health-file defaults** repo for L337-org.
It has no application code, no dependencies, and no CI — just the markdown files below plus
the org's public profile page. It is not a mirror of another repo's instructions file; unlike
`docker-mcp` and `send-to-influx`, there is no paired `CLAUDE.md` for this one to track.

## Files

- **`CONTRIBUTING.md`** / **`SECURITY.md`** — GitHub uses these as the **fallback** shown on any
  org repo that has no file of its own name at its own root (or `.github`/`docs`) — e.g. on the
  repo's "Health" tab, its `/community` page, and the "Report a vulnerability" flow. Both files
  say this explicitly and say a repo's own copy takes precedence. Keep them **generic** — org-wide
  process (branch/PR flow, where to report a vulnerability), never a specific project's setup
  steps or checklists. A repo-specific detail belongs in that repo's own file, not here.
- **`profile/README.md`** — renders as the org's public profile at github.com/L337-org. Read by
  visitors, not by tooling. Keep the project table current when a repo is added, renamed, or its
  status/badges change; don't let it drift out of sync with what actually exists in the org.
- **This file** (`.github/copilot-instructions.md`) and **`CODEOWNERS`** — read by Copilot's PR
  review and by GitHub's review-request routing, same as in any other repo. GitHub does not
  support inheriting either of these org-wide, so every repo — including this one — carries its
  own; there is no fallback semantics here the way there is for `CONTRIBUTING.md`/`SECURITY.md`.

## Branch policy — same as the org's other repos

Pull Requests were disabled as a repository feature on this repo until 2026-08-11 (a leftover from
however it was originally set up, not a GitHub platform restriction on `.github` repos generically
— `github/.github` and plenty of other orgs' `.github` repos have PRs on). `main`'s ruleset already
required signed commits and blocked force-push/deletion; now that PRs are enabled, it carries the
same PR-required/squash-only/code-owner-review/Copilot-review shape as every other repo in the org.
There is no standing carve-out for this repo — treat it the same as `docker-mcp`/`send-to-influx`/
`apt`/`homebrew-tap` for branch policy purposes.
