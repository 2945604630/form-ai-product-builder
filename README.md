# FORM — AI Product Builder

**Turn vague ideas into buildable products.**

FORM is a local-first product workbench for creators using Codex, ChatGPT, Obsidian, and AI coding tools. It turns a vague idea into a structured project package: Idea Canvas, Feature Decision, PRD, User Flow, UI Direction, Technical Plan, Build Pack, and Iteration Instructions.

## Features
- Project creation, editing, search, duplicate, archive, delete with confirmation, progress and next-step hints.
- Complete sample project: English Vocabulary Learning Assistant.
- Editable Idea Canvas with Local Template Mode preview/accept flow.
- Feature Decision system with Must/Should/Could/Later/Rejected, filtering, and value/cost suggestion.
- PRD Workspace with locked sections, generation, restore, and copy.
- Structured User Flow editor that emits Mermaid Markdown.
- Editable UI Direction and Technical Plan.
- Build Pack generation for `project-brief.md`, `prd.md`, `feature-scope.md`, `interaction-flow.md`, `design-system.md`, `technical-plan.md`, `data-model.md`, `acceptance-criteria.md`, `AGENTS.md`, `codex-master-prompt.md`, and `tasks.md`.
- Iteration Instructions converting natural language requests into Codex-ready instructions.
- Settings for theme, language, OpenAI-compatible provider fields, Local Template Mode, JSON backup/restore, and reset.

## Tech Stack
React, TypeScript, Vite, Zustand, Dexie, Zod, JSZip, Lucide React, Vitest, ESLint.

## Commands
```bash
npm install
npm run dev
npm run typecheck
npm run lint
npm run test
npm run build
```

## AI Configuration
The product works fully without an API key in Local Template Mode. Optional API settings are user-provided and local. Do not commit real API keys; `.env.example` documents optional defaults only.

## Local Data
Projects and settings are saved in browser IndexedDB. Use Settings → Backup JSON and Restore Data for portable backups. Invalid backup JSON is rejected with an error message.

## Export
Single Markdown files and ZIP Build Pack downloads are supported through browser Blob downloads.

## Directory Structure
- `src/types` — domain model.
- `src/data` — defaults and sample project.
- `src/services` — generator/export/AI abstractions.
- `src/store` — Dexie + Zustand local-first state.
- `docs` — planning documents.
