<p align="center"><img src="https://raw.githubusercontent.com/cecilusmax33/cecilusmax33/main/assets/logos/code-bro-one-logo.png" alt="Code-Bro-One logo" width="220"></p>

# Code Bro One — Technical Blueprint

Design blueprint for **Code Bro One**, an autonomous multi-agent software development lifecycle (SDLC) platform: describe an app, and a council of specialized AI agents architects, builds, styles, tests, and deploys it.

## The design in one page

- **The Orchestrator** — a Supervisory LLM gateway that ingests raw code, UI mockups, and text specs; normalizes them into a JSON project manifest; runs a validation loop (asks clarifying questions before any agent executes); and dispatches work through a state-machine hand-off protocol (IDLE → PARSING → VALIDATING → ARCHITECTING → BUILDING → STYLING → DEBUGGING → DEPLOYING).
- **The Agentic Council** — five agents, each with *immutable directives* that user prompts cannot override:
  1. **The Architect** (structure) — folder hierarchy, dependency trees, API schemas; never writes business logic
  2. **The Builder** (logic) — pure code generation, bound to the Architect's schema, strict type safety
  3. **The Stylist** (UI/UX) — wireframes/prompts → Tailwind or React Native, mobile-first, WCAG AA
  4. **The Debugger** (QA) — linting, unit tests, security scans; zero tolerance for critical/high vulnerabilities, auto-rollback
  5. **The Deployer** (launch) — packages into the isolated **PwnBox** sandbox and generates a temporary PWA URL + QR code for mobile viewing
- **Companion Launch Studio** — split-screen terminal/preview with live agent logs, preset template "pills," and persistent context via SQLite + a vector database (Pinecone/pgvector).
- **PwnBox deployment** — Docker/WebContainers sandbox with Node/Python/Go runtimes, exposed to a phone through a secure tunnel (Ngrok-style relay) and a dynamic QR code.

## Contents

| File | What it is |
| --- | --- |
| `Code-Bro-One-Technical-Blueprint.md` | The full blueprint: the original architecture prompt plus the complete generated specification, including the agent hand-off sequence diagram and API spec |

## Provenance

Produced in a Gemini session (linked at the top of the blueprint document) and exported as Word/PDF. This repo holds the Markdown conversion so the text is searchable and version-controlled; the original `.docx` and `.pdf` binaries are unchanged in the owner's files.
