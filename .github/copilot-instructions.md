<!-- .github/copilot-instructions.md -->
# Copilot / AI Agent Instructions — Linux_Cmd

Purpose
- Help an AI coding or documentation agent become productive quickly in this repository.

Repository snapshot (big picture)
- This repository is a collection of Linux & networking notes and short architecture write-ups — there is no build system or source code. Key files: [README.md](README.md), [linux.md](linux.md), [DROVE.md](DROVE.md), [Networking_knw.txt](Networking_knw.txt).

What an agent should assume
- Changes are primarily documentation: add/clarify command examples, expand explanation sections, and preserve existing formatting (code fences, ASCII diagrams, and hand-formatted lists).
- There is no automated CI, tests, or package manifest in the repo root; do not introduce expectations for build tooling unless the user asks.

Editing patterns and conventions (project-specific)
- File naming: existing files use lowercase names with underscores or plain names (e.g., linux.md). Follow the same style for new files.
- Markdown style: use fenced code blocks with language tags (````bash```) for command examples — see [linux.md](linux.md) for the canonical curl options block.
- Preserve ASCII diagrams and custom formatting (see architecture block in [DROVE.md](DROVE.md)). Don't reflow or rewrap those sections.
- Short topical files: prefer small, focused files per topic (networking, container orchestration, command cheatsheets).

How to add or extend content (examples)
- Adding a new command section in `linux.md`:
  - Add a second-level header: `## <command>`
  - Provide a one-line summary, then a short flagged list and a `bash` code block with 1–3 common examples.
  - Follow the curl-section layout: grouped headings, then a compact table/list of flags.

- Updating `DROVE.md` architecture notes:
  - Keep the ASCII architecture line and add small clarifying bullets beneath it. If you must restructure, keep the original as a quoted block and add an improved summary above or below.

Safety checks before committing
- Preview markdown locally (editor preview) to ensure code fences and diagrams render as intended.
- Do not rename or reformat existing docs en masse — small, incremental edits are preferred.

When to ask the user for clarification
- If a proposed change converts a plaintext note (e.g., `Networking_knw.txt`) into a structured guide or tutorial — ask whether they want a full rewrite or a minimal edit.
- If adding tooling or CI (linters, spellcheckers, formatters), ask first — the repo currently contains only raw notes.

Files to check for related context
- [README.md](README.md) — repository entry (currently empty). Update this if you add or reorganize major topics.
- [linux.md](linux.md) — canonical command/flags examples (use as template).
- [DROVE.md](DROVE.md) — architecture/diagrams; preserve formatting.
- [Networking_knw.txt](Networking_knw.txt) — plaintext networking notes.

If you make a larger change
- Summarize edits at the top of the PR or commit message as: `docs: <short summary> — updated <file1>, <file2>` so humans can quickly review documentation-only updates.

Questions or feedback
- If any section is ambiguous or you want a different level of restructuring (convert notes into tutorials, add links, or introduce CI), ask before proceeding.
