# NovaSpire AI — Enterprise Cognitive AI Platform

> Deterministic. Auditable. Controllable. Open Source.

---

## Overview

**NovaSpire AI** is an enterprise-grade cognitive AI platform built without dependency on external LLMs. It provides a proprietary hybrid reasoning engine, a deterministic 14-stage cognitive pipeline, and a unified knowledge layer designed for regulated industries and production environments.

This is the open source release of NovaSpire AI, featuring the complete cognitive intelligence engine with modular architecture, autonomous learning capabilities, and a multi-agent coding system.

---

## 🚀 Quick Start

```bash
# 1. Clone
git clone https://github.com/your-org/condrox-ai.git
cd condrox-ai

# 2. Install dependencies
pip install -r requirements.txt

# 3. Configure
cp config/system.yaml.example config/system.yaml
# Edit config/system.yaml — set environment, ports, etc.

# 4. Start the API server
python -m uvicorn api.main:app --host 0.0.0.0 --port 8000
# API available at http://localhost:8000/api/v1
# Interactive docs at http://localhost:8000/docs
```

---

## 📁 Project Structure

```
condrox-ai/
├── core/               Core systems (reasoning, memory, learning, security, audit, kernel)
├── api/                FastAPI server (v1 endpoints, auth, middleware)
├── pipeline/           14-stage deterministic cognitive pipeline
├── agents/             Modular cognitive agents (including IDE-MASTER-V2 CodingTeam)
├── knowledge/          Unified knowledge layer (YAML, SQL, vector)
├── data/               Raw, processed, logs, cache
├── config/             System configuration (YAML)
├── docs/               Architecture, API, security, compliance documentation
├── Frontend/           Chat interface, admin dashboard, and NovaSpire IDE
├── SingleTraining/     Enterprise training system for massive content generation
├── tests/              Unit, integration, pipeline, security, performance tests
├── deploy/             Docker, Kubernetes, CI/CD configurations
├── tools/              Diagnostics, migration, refactoring utilities
└── workspace-rules.md  Project structure and organization rules
```

---

## ⚙️ Configuration

All configuration lives in `config/`:

| File | Purpose |
|---|---|
| `system.yaml` | Global runtime settings |
| `security.yaml` | RBAC, authentication, threat detection |
| `memory.yaml` | Memory system settings |
| `learning.yaml` | Knowledge learning settings |
| `api.yaml` | API server and endpoint settings |

---

## 🌟 Key Features

### Cognitive Intelligence Engine
- **14-Stage Deterministic Pipeline** — Fixed cognitive processing order with auditable outputs
- **Hybrid Reasoning** — Chain-of-thought, multi-turn, and meta-reasoning capabilities
- **Knowledge Layer** — Unified YAML, SQL, and vector backends with semantic search
- **Memory System** — Episodic, semantic, procedural, and long-term memory types

### Autonomous Learning
- **Background Knowledge Ingestion** — Continuous learning from Wikipedia and arXiv
- **Domain Growth Engine** — Automatic knowledge base expansion
- **Self-Correction Engine** — Conflict resolution and quality improvement
- **Cross-Domain Reasoning** — Knowledge transfer between domains

### Multi-Agent Coding System
- **IDE-MASTER-V2** — Five specialist agents for autonomous software development
- **PlannerAgent** — Task decomposition and architecture selection
- **CoderAgent** — Code generation and project scaffolding
- **DebuggerAgent** — Bug detection and root cause analysis
- **AnalystAgent** — Code quality and consistency review
- **DocumenterAgent** — Automatic documentation generation

### Enterprise Training System
- **Massive Content Generation** — Academy-level training content at scale
- **Quality Assurance** — Multi-dimensional quality checks and peer review
- **Concurrent Processing** — Parallel batch processing for efficiency
- **Topic Expansion** — Infinite compound topic generation

### Security & Compliance
- **RBAC** — Role-based access control
- **Input Validation** — Comprehensive threat detection and injection scanning
- **Audit Logging** — Complete decision traceability
- **GDPR Ready** — Privacy-first design with data minimization

---

## 🎯 Use Cases

- **Enterprise Knowledge Management** — Structured knowledge base with semantic search
- **Autonomous Software Development** — AI-assisted coding with multi-agent coordination
- **Professional Training** — Academy-level content generation at scale
- **Regulated Industries** — Deterministic, auditable AI for healthcare, finance, legal
- **Research & Development** — Knowledge extraction and synthesis from academic sources

---

## 📚 Documentation

| Document | Location |
|---|---|
| Architecture overview | `docs/architecture/overview.md` |
| 14-stage pipeline | `docs/pipeline/pipeline.md` |
| Security framework | `docs/architecture/security-framework.md` |
| Memory system | `docs/architecture/memory-system.md` |
| Knowledge layer | `docs/architecture/knowledge-layer.md` |
| Learning system | `docs/architecture/learning-system.md` |
| API documentation | `docs/api/` |
| Testing guide | `docs/testing/overview.md` |

---

## 🧪 Testing

```bash
# Run all tests
pytest

# Run specific test suites
pytest tests/unit/
pytest tests/integration/
pytest tests/security/

# Run with coverage
pytest --cov=core --cov=api --cov=pipeline
```

---

## 🐳 Docker Deployment

```bash
# Build image
docker build -t condrox-ai:latest -f deploy/docker/Dockerfile .

# Run container
docker run -p 8000:8000 -v $(pwd)/data:/app/data condrox-ai:latest
```

---

## 🤝 Contributing

We welcome contributions! Please read our contribution guidelines:

1. Read [`workspace-rules.md`](workspace-rules.md) — folder structure, naming conventions
2. Read [`workspace-policy.md`](workspace-policy.md) — coding standards and deployment policy
3. Fork the repository
4. Create a feature branch
5. Make your changes with tests
6. Submit a pull request

### Development Setup

```bash
# Install development dependencies
pip install -r requirements.txt
pip install -r requirements-dev.txt

# Run pre-commit hooks
pre-commit install

# Run type checking
mypy core/ api/ pipeline/

# Run linting
ruff check core/ api/ pipeline/
```

---

## 📊 Performance

- **Pipeline SLA**: <1,160ms total (14 stages)
- **Memory Access**: <50ms average retrieval
- **Knowledge Search**: <100ms semantic search
- **Concurrent Processing**: 4+ parallel workers
- **Quality Gates**: 0.60+ threshold enforcement

---

## 🔒 Security

- **No External LLM Dependencies** — Fully self-contained
- **Deterministic Outputs** — Same input always produces same output
- **Complete Audit Trail** — Every decision logged and traceable
- **Threat Detection** — Injection scanning, PII detection, command injection prevention
- **Rate Limiting** — 60 requests/min per user
- **JWT Authentication** — 24-hour token expiry

---

## 🗺️ Roadmap

### v1.4.0 (Q3 2026)
- Enhanced multi-modal reasoning
- Improved knowledge graph visualization
- Extended agent capabilities

### v1.5.0 (Q4 2026)
- Federated learning support
- Advanced anomaly detection
- Performance optimization

### v2.0.0 (2027)
- Distributed cognitive processing
- Enhanced autonomous learning
- Industry-specific templates

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

Copyright (c) 2026 Condrox AI Contributors

---

## 🙏 Acknowledgments

- Built with Python 3.11+, FastAPI, and Pydantic v2
- Inspired by cognitive science and enterprise AI requirements
- Community feedback and contributions

---

## 📞 Support

| Channel | Contact |
|---|---|
| GitHub Issues | https://github.com/your-org/condrox-ai/issues |
| Discussions | https://github.com/your-org/condrox-ai/discussions |
| Documentation | https://docs.condrox.ai |

---

## 🌟 Star History

If you find NovaSpire AI useful, please consider giving it a star on GitHub!

---

**Built with ❤️ by the Condrox AI Community**
