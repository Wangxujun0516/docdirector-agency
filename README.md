# DocDirector Agency

The **AI-powered technical documentation company.** A starter package of agent definitions, skills, and workflows that turn documentation requests into published, reviewed, and maintained documents — with the human writer as creative director.

## Overview

DocDirector Agency is a structured set of **9 specialized agents**, **8 reusable skills**, and **4 workflow definitions** that orchestrate the full documentation lifecycle: research, outlining, drafting, code examples, visualization, multi-pass review, maintenance monitoring, and analytics.

## Quick Demo

Here's what the agency produced when given a one-sentence brief: *"Document a POST /api/v1/translations endpoint for a translation API. Target audience: frontend engineers."*

The output included a full API reference with parameters, error handling, rate limits, examples in cURL/Node.js/Python, and a Mermaid sequence diagram — all produced by routing through the Research → Outline → Draft → Code Sample → Review pipeline. [See the full output in the live demo.](#)

## Package Structure

```
docdirector-agency/
├── COMPANY.md              # Company mission, philosophy, and agent/skill index
├── TEAM.md                 # Team structure, reporting, and handoff protocols
├── LICENSE                 # MIT license
├── agents/                 # Agent definitions
│   ├── director/AGENTS.md    # Orchestrator, quality gate
│   ├── researcher/AGENTS.md  # Source investigation
│   ├── outliner/AGENTS.md    # Information architecture
│   ├── drafter/AGENTS.md     # First full draft
│   ├── codesample/AGENTS.md  # Verified code examples
│   ├── visualizer/AGENTS.md  # Mermaid + diagrams
│   ├── reviewer/AGENTS.md    # Multi-pass quality check
│   ├── maintainer/AGENTS.md  # Staleness monitoring
│   └── analyst/AGENTS.md     # Coverage & quality metrics
├── skills/                 # Reusable skill instructions
│   ├── doc-research/SKILL.md
│   ├── api-doc-generation/SKILL.md
│   ├── style-guide-enforcement/SKILL.md
│   ├── hallucination-detection/SKILL.md
│   ├── freshness-monitoring/SKILL.md
│   ├── mermaid-diagram-generation/SKILL.md
│   ├── user-empathy-mapping/SKILL.md
│   └── review-and-quality/SKILL.md
├── workflows/              # Process flows
│   ├── standard-doc-lifecycle.md
│   ├── new-api-endpoint.md
│   ├── full-product-guide.md
│   └── maintenance-sweep.md
├── style-guide.md          # Shared voice, tone, formatting rules
└── README.md               # This file — installation and usage
```

## Usage

### Creating a new document

1. Engage the **Documentation Director** with a description of what's needed.
2. The Director decomposes the request and routes it through the appropriate workflow.
3. Agents execute their roles — research, outline, draft, add code samples, visualize, review.
4. The Human Director approves or iterates.
5. The finished document is published and registered for freshness monitoring.

### Available Workflows

| Workflow | Trigger | Output |
|---|---|---|
| `standard-doc-lifecycle` | General doc request | Full lifecycle from intake to delivery |
| `new-api-endpoint` | API endpoint spec or PR | API reference with tested examples |
| `full-product-guide` | New feature or major release | Comprehensive user guide |
| `maintenance-sweep` | Code changes / scheduled scan | Updated docs with freshness report |

### Adding new skills

Add a directory under `skills/<skill-name>/` with a `SKILL.md` containing frontmatter (name, description, version) and instructions organized by process steps.

### Adding new agents

Add a directory under `agents/<role-name>/` with an `AGENTS.md` containing frontmatter (schema, name, role, reports_to, skills), then responsibilities, input, output, and workflow position.

## Prerequisites

- Definition-only: no runtime dependencies.
- Consumed by AI coding agents (Codex, etc.) via the agent definition and skill files.

## License

MIT — see [LICENSE](LICENSE).

## Contributing

New additions should follow the existing patterns:
- One responsibility per agent.
- Skills are reusable across agents and workflows.
- Workflows define explicit handoffs and success criteria.
- All definitions use YAML frontmatter per `schema: agentcompanies/v1`.
