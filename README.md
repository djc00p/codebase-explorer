# 🗺️ Codebase Explorer

[![ClawHub Skill](https://img.shields.io/badge/ClawHub-Skill-blue)](https://clawhub.ai/djc00p/codebase-explorer) [![Agent Skill](https://img.shields.io/badge/Agent-Skill-blue)](#) [![Onboarding](https://img.shields.io/badge/Onboarding--Guides-green.svg)](https://en.wikipedia.org/wiki/Onboarding) [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

**Codebase Explorer** systematically analyzes unfamiliar repositories and produces structured onboarding guides — architecture maps, entry points, conventions, and a ready-to-use `CLAUDE.md`.

Reading a codebase by opening files one at a time is slow and misses the structure that makes a project make sense. This skill works the way a good senior engineer does on day one: identify the stack, map the directories, trace one request end to end, learn the conventions, then write it down.

---

## 🎯 When to Use

* First time opening a project
* Joining a new team or repository
* *"Help me understand this codebase"*
* *"Generate a CLAUDE.md for this project"*
* *"Onboard me"* / *"Walk me through this repo"*

---

## 🚀 Quick Start

1. **Scan manifests and config** — identify tech stack and framework
2. **Map directory structure and entry points** — top 2 levels
3. **Trace one request lifecycle** — entry → validation → business logic → database
4. **Identify conventions** — naming, error handling, async patterns, testing
5. **Generate the artifacts** — onboarding guide + starter `CLAUDE.md`

---

## 🔍 Key Concepts

* **Reconnaissance** — file presence patterns reveal the tech stack (`package.json`, `Gemfile`, `go.mod`, `requirements.txt`)
* **Architecture pattern** — monolith vs. monorepo, frontend/backend split, API style
* **Convention detection** — extract naming, error handling, and async patterns from *recent* code, not just any code
* **Guided exploration** — don't read everything; use grep/glob selectively to resolve ambiguity
* **Two-artifact output** — an onboarding guide (structure + conventions) *and* a `CLAUDE.md` (project instructions)

---

## 🧭 The Five Phases

### Phase 1 — Reconnaissance

Detect the stack from file presence before reading any code:

| Look for | Means |
|----------|-------|
| `package.json` + `tsconfig.json` | TypeScript/Node |
| `Gemfile` + `config/routes.rb` | Ruby on Rails |
| `go.mod` | Go |
| `requirements.txt` / `pyproject.toml` | Python |
| `Cargo.toml` | Rust |
| `pnpm-workspace.yaml` / `turbo.json` | Monorepo |

### Phase 2 — Architecture Map

Directory structure, top 2 levels, entry points, and the monolith-vs-monorepo call.

### Phase 3 — Request Lifecycle

Trace **one** request fully: entry → validation → business logic → database. This single trace reveals the layering conventions better than reading a hundred files.

### Phase 4 — Convention Detection

Naming, error handling, async patterns, and test structure — sampled from recent commits so you learn the conventions as they are *now*, not as they were three years ago.

### Phase 5 — Artifacts

Two outputs, each with a distinct audience:

**Onboarding guide** — for humans joining the team: overview, tech stack, architecture, key entry points, directory map, request lifecycle, conventions, common tasks, where to look.

**`CLAUDE.md`** — for agents working in the repo: tech stack, code style, testing, build & run commands, project structure, conventions, best practices, anti-patterns to avoid.

---

## 📚 References

* `references/reconnaissance.md` — file patterns for framework and language detection
* `references/artifacts.md` — onboarding guide and `CLAUDE.md` templates, best practices, anti-patterns

---

**Adapted from [everything-claude-code](https://github.com/affanm/everything-claude-code) by [@affaan-m](https://github.com/affaan-m) (MIT).**

**Published by [@djc00p](https://github.com/djc00p)**
