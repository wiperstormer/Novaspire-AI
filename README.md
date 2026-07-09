# NovaSpire AI — Powered by CHCIE

> Enterprise Cognitive AI Platform — Deterministic. Auditable. Controllable.
> Size 12 GB

---

## Overview

**NovaSpire AI** is the flagship intelligent assistant powered by the **Condrox Hybrid Cognitive Intelligence Engine (CHCIE)**. It is a self-contained, enterprise-grade cognitive AI platform built without dependency on external LLMs. CHCIE provides a proprietary hybrid reasoning engine, a deterministic 14-stage cognitive pipeline, and a unified knowledge layer designed for regulated industries.

This repository contains both the NovaSpire AI product experience and the CHCIE engine underneath.

---

## Quick Start

```bash
# 1. Clone
git clone https://github.com/your-org/condrox-ai.git
cd condrox-ai

# 2. Install dependencies
pip install -r requirements.txt

# 3. Configure
cp config/system.yaml.example config/system.yaml
# Edit config/system.yaml — set environment, ports, etc.

# 4. Start
python -m uvicorn api.main:app --host 0.0.0.0 --port 8000
# API available at http://localhost:8000/api/v1
# Docs at http://localhost:8000/docs
```

---

## Project Structure

```
condrox-ai/
├── core/               Core systems (reasoning, memory, learning, security, audit, kernel)
├── api/                Single FastAPI server (v1 endpoints, auth, middleware)
├── pipeline/           14-stage deterministic cognitive pipeline
├── agents/             Modular cognitive agents (including IDE-MASTER-V2 CodingTeam)
├── knowledge/          Unified knowledge layer (YAML, SQL, vector)
├── data/               Raw, processed, logs, cache
├── config/             All system configuration (YAML)
├── docs/               Architecture, API, security, compliance, roadmap, investor, upgrades
├── Frontend/           Chat interface, admin dashboard, and NovaSpire IDE
├── DesktopApp/         Optional desktop wrapper for the IDE
├── tests/              Unit, integration, pipeline, security, performance
├── deploy/             Docker, Kubernetes, CI/CD
├── tools/              Diagnostics, migration, refactoring
├── workspace-rules.md  Project structure and organisation rules
└── workspace-policy.md Coding standards, naming, deployment policy
```

---

## Configuration

All configuration lives in `config/`:

| File | Purpose |
|---|---|
| `system.yaml` | Global runtime settings |
| `security.yaml` | RBAC, auth, threat detection |
| `memory.yaml` | Memory system settings |
| `learning.yaml` | Knowledge learning settings |
| `api.yaml` | API server and endpoint settings |

---

## What's New in v1.1.0

### Conversational Intelligence
- **CPIE-1** — warm, human-like personality with adaptive tone and dialogue flow
- **FCP-1** — friendly openers, transitions, closers, micro-pauses, and energy matching
- **MSR-1** — durable user memory: "remember I love pizza" → "You love pizza."
- **ECM-6** — curiosity engine with context-aware follow-up questions

### Knowledge Scale & Quality
- **KU-1** — hierarchical knowledge universe (category → subnode → section)
- **KVE-1** — continuous knowledge audit, validation, and quality scoring
- Knowledge search now returns structured universe nodes for deep topics

### Reliability & Operations
- **PM-1** — cross-platform single-instance enforcement
- **PM-2** — conversational inputs no longer blocked by quality gates
- Robotic phrases like "Please note that" are automatically stripped

See full release notes in `docs/releases/v1-1-0.md` and `CHANGELOG`.

---

## What's New in v1.3.0

### Intelligence Stack
- **Meta-Learning Engine (MLE-1)** — adaptive strategy selection based on past outcomes
- **Evaluation & Benchmarking Engine (EVAL-1)** — deterministic benchmarks and regression tracking
- **Intelligence Metrics (IM-1)** — reasoning depth, abstraction, generalization, transfer, learning efficiency, knowledge alignment
- **Intelligence Governance (IG-1)** — quality gates and regression protection
- Extended **Component System** with `meta_learning` and `evaluation` components

---

## New Capabilities

### NovaSpire IDE (Frontend/IDE)
A full-featured browser-based IDE for NovaSpire AI-assisted software development:
- Draggable panels with VS Code-like grid layout
- File explorer with list/grid views, folder expand/collapse
- Code editor with synced line numbers
- Live preview panel with console capture
- AI chat panel with command hints and streaming responses
- Settings modal for AI backend URL/token
- Direct integration with the CHCIE backend API

Start it with:

```bash
cd Frontend/IDE
npm install
npm run dev
```

### IDE-MASTER-V2 Multi-Agent Coding Engine
The `CodingOrchestrator` coordinates five specialist agents for autonomous coding:
- **PlannerAgent** — breaks tasks into steps and selects architecture
- **CoderAgent** — generates code, scaffolds projects, edits files
- **DebuggerAgent** — finds bugs, explains root cause, suggests fixes
- **AnalystAgent** — reviews project consistency and quality
- **DocumenterAgent** — generates README, API docs, and comments

Invoked automatically for intents: `CODE_GENERATE`, `CODE_REVIEW`, `TEST_GENERATE`, `DEBUG`, `REFACTOR`, `OPTIMIZE`, `PLAN`, `DOCUMENT`.

### Kernel Component System (CS-1)
Boots and supervises NovaSpire AI / CHCIE subsystems in separate processes:
- `api_server` — CHCIE FastAPI server
- `learning_worker` — background autonomous learning worker
- `autonomous_learning` — periodic classifier retraining and graph maintenance
- `meta_learning` — strategy optimization
- `evaluation` — scheduled benchmarks and governance checks

Each component runs in isolation; crashes are contained and restarted. Start with:

```bash
python start_ai.py
```

### FIX-INTENT-V1 Strict Domain Lock
Domain and topic lock prevents drift during conversations:
- First meaningful query sets the locked domain
- Continuation phrases (`tell me more`, `continue`, `go deeper`) stay within topic
- Explicit reset phrases (`no, I mean...`) switch domain and reset lock
- Knowledge retrieval is restricted to the locked domain
- Quality evaluator rejects off-domain responses
- Medical (`Health`) domain never falls back to AI/ML or generic answers

### Autonomous Learning v2–v8
Upgraded learning modules are documented in `docs/upgrade/autonomous-learning-upgrade-v2-v8.md`:
- v2 Topic Expansion
- v3 Auto-KB Integration
- v4 Domain Growth Engine
- v5 Self-Correction Engine
- v6 Cross-Domain Reasoning Engine
- v7 Concept Fusion Engine
- v8 Safety-Aware Learning Engine

---

## Documentation

| Document | Location |
|---|---|
| Architecture overview | `docs/architecture/overview.md` |
| 14-stage pipeline | `docs/pipeline/14-stage-loop.md` |
| Security framework | `docs/architecture/security-framework.md` |
| GDPR compliance | `docs/compliance/gdpr.md` |
| EU AI Act | `docs/compliance/eu-ai-act.md` |
| Product roadmap | `docs/roadmap/2026-2030.md` |
| Investor whitepaper | `docs/investor/whitepaper.md` |
| v1.1.0 Release Notes | `docs/releases/v1-1-0.md` |
| CHCIE System Identity | `System.md` |
| Startup guide | `docs/STARTUP_GUIDE.md` |
| Debug analysis report | `docs/DEBUG_ANALYSIS_REPORT.md` |
| IDE README | `Frontend/IDE/README.md` |
| Domain lock spec | `docs/upgrade/domain-lock-v1.md` |
| Autonomous Learning upgrade | `docs/upgrade/autonomous-learning-upgrade-v2-v8.md` |
| Intelligence Stack roadmap | `docs/upgrade/intelligence-stack-upgrade-roadmap.md` |

---

## Key Principles

- **Determinism** — same input always produces same output
- **Auditability** — every decision is logged and traceable
- **Modularity** — single responsibility per module, clean interfaces
- **Security-first** — RBAC, validation, threat detection at every layer
- **No legacy debt** — clean architecture, no duplicate modules
- **Autonomous Learning** — background knowledge ingestion from Wikipedia and arXiv
- **Intelligence Stack** — meta-learning, evaluation, metrics, and governance

---

## Workspace Rules

Before contributing, read:
- [`workspace-rules.md`](workspace-rules.md) — folder, file, naming, pipeline, memory, knowledge, security, audit rules
- [`workspace-policy.md`](workspace-policy.md) — coding standards, module isolation, deployment policy

---

## License

Open Source and free of charge

## Support

Created by Tobias Østen
Tobias@rubiconmedia.no

Leave the prosject as it is. Ai needs traning and some patching and its ready to go.
