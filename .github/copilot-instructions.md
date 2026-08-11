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

## Branch policy — deliberately different from the org's other repos

`main` here has **no PR-required ruleset**. It keeps a ruleset requiring signed commits and
blocking force-push/deletion, but nothing gates a direct push with review or CI. This is a
deliberate, standing exception (not an oversight to "fix" to match `docker-mcp`/`send-to-influx`):
this repo holds policy and profile text that benefits from fast, direct edits, not the
squash-merge-plus-review flow that makes sense for code changes elsewhere in the org. Opening a PR
here is still fine and often useful for visibility, but never propose or add a PR-required
ruleset to this repo — that would work against the reason it's set up this way.
