# CLAUDE.md

Guidance for Claude Code when working in this repository.

## Project Overview

Claude Code Deep Dive Workshop — a Korean-language training curriculum distributed as rendered PDF slide decks plus a searchable markdown archive of every code example. This is a **content repository**: no build system, no tests, no application code.

## Repository Layout

- `20260525/`, `20260703/` — chapter PDFs, one directory per curriculum edition (date-stamped `YYYYMMDD`). `20260703/` is the latest edition, newly authored against Claude Code 2.1.198. Six chapters per edition: Ch1 Overview, Ch2 Agents & Subagents, Ch3 Admin Setup, Ch4 Settings, Ch5 CLI Reference, Ch6 Agent SDK.
- `tech_doc/` — supplementary technical documents (`ClaudeCode-Architecture.pdf`, `Claude_Cost_Efficiency.pdf`), kept separate from the chapter curriculum.
- `Script/workshop-code/` — 502 extracted code snippets as markdown, organized `chN-topic/part-NN-slug/NNN-slug.md` where `NNN` is the source slide number. Each file contains the slide title, the code block, and a Korean speaker note.
- `README.md`, `CHANGELOG.md` — bilingual documents (English section first, Korean second).

## Conventions

- **PDFs are rendered artifacts — never edit them.** They are regenerated from source decks maintained outside this repository.
- Snippet filenames follow `NNN-meaningful-slug.md` (`NNN` = slide number). Keep numbering stable. When changing snippet content, cite the source slide number in the commit body.
- Bilingual docs: identical structure in both language sections. Language toggle uses HTML `<a href="#english"><img ...></a>` badges with ASCII anchors and explicit `<a id="english">` / `<a id="korean">` tags — not Markdown badge links. No emojis in documents.
- Changelog entries: English imperative ("Add X") / Korean 명사형 종결 ("X 추가"). Category headings stay in English in both sections.
- Do not mention AWS organization or standard names (AWS Korea, V-team, AWS PPT template, AWS Confidential) in documents; use neutral wording such as "consistent design system" and "Proprietary" license.
- Commits follow Conventional Commits (`feat:`, `fix:`, `docs:`, `refactor:`, `chore:`).
- Ignore `.DS_Store` files; they are macOS artifacts.

## Common Tasks

```bash
# Find snippets by keyword
grep -rn "PreToolUse" Script/workshop-code/

# Find snippets by filename
find Script/workshop-code/ -name "*auth*"

# List snippets in a part
ls Script/workshop-code/ch6-sdk/part-01-sdk-basics/
```
