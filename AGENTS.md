# AGENTS.md

Handbook for automated and interactive coding agents working in this repository.

## Rules

- **Repo Scope**: This repository (`kleosr/kleosr`) is a GitHub profile repository centered on `README.md` and branding assets in `assets/`.
- **Minimal Changes**: Only touch files explicitly relevant to profile content, branding assets, and agent instructions. Do not add arbitrary application dependencies or runtime code.
- **Git Hygiene**:
  - Respect existing branch conventions and commit message styles.
  - Never commit untracked temporary files (e.g., `*.bat`, `branch_structure.json`). Respect `.gitignore`.
  - Do not force push or delete remote branches unless explicitly instructed.
- **Automation Settings**:
  - Maintain `.vscode/settings.json` configuration (`task.allowAutomaticTasks: "off"`). Do not enable automated tasks without explicit authorization.
- **Assets Integrity**:
  - Maintain SVG assets in `assets/` (light and dark mode pairs: `cursor-light.svg` / `cursor-dark.svg`, `spacexai-light.svg` / `spacexai-dark.svg`).
  - When referencing assets in `README.md`, ensure dark/light variants follow the `#gh-light-mode-only` and `#gh-dark-mode-only` hash anchors.

## Skills

Reusable task recipes belong in `.agents/skills`.
- The repository does not currently define local task skills.
- When creating skills in the future, place them in `.agents/skills/<skill-name>/` with a clear interface and prerequisites.

## Workflows

- **Profile Maintenance**:
  - Edits to `README.md` must preserve valid Markdown and HTML alignment structures (`<div align="center">...</div>`).
  - Verify all external links (`github.com/kleosr/*`, `x.com/kleosrr`).
- **Asset Updates**:
  - Brand badges and SVGs added to `assets/` should provide both light and dark themes where applicable.
  - Verify rendering in both GitHub themes.
- **Verification**:
  - No automated build or test toolchain is currently configured for this repository.
  - Proof of work: inspect git diff (`git diff`), verify file syntax and links, ensure working tree is clean.

## Memory

- Versioned memory and documentation belong under `docs/`.
- The repository currently does not contain a `docs/` directory or existing agent memory files.
- Never rely on vendor-proprietary memory features; keep any persistent agent context versioned in Git when introduced.
