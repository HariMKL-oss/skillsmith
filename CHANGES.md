# Changes in this fork

Skillsmith is derived from Anthropic's `skill-creator` example skill
(Apache-2.0). Per the license, this file records the notable changes.

## Renaming and packaging
- Renamed the skill from `skill-creator` to `skillsmith` (frontmatter `name`,
  document title, and internal self-references).
- Rewrote the `description` for more reliable triggering (covers building,
  editing, testing, benchmarking, description-optimization, and packaging,
  and triggers even when the user doesn't say the word "skill").
- Added repository scaffolding for public distribution: `README.md`,
  `NOTICE`, this `CHANGES.md`, and `.gitignore`.

## Unchanged
- The core workflow and all bundled resources (`agents/`, `eval-viewer/`,
  `references/`, `scripts/`, `assets/`) are carried over from the original so
  the skill keeps working across Claude Code, Cowork, and Claude.ai.

> If you make further edits, add them here so downstream users (and the
> license) stay honest.
