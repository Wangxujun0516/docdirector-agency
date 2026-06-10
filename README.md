# DocDirector Agency

The **AI-powered technical documentation company.** A starter package of agent definitions, skills, and workflows that turn documentation requests into published, reviewed, and maintained documents — with the human writer as creative director.

**Current version:** [v0.1.0](https://github.com/Wangxujun0516/docdirector-agency/releases/tag/v0.1.0) — Initial release.

## Overview

DocDirector Agency is a structured set of **9 specialized agents**, **8 reusable skills**, and **4 workflow definitions** that orchestrate the full documentation lifecycle: research, outlining, drafting, code examples, visualization, multi-pass review, maintenance monitoring, and analytics.

## Live Demo

Given this one-sentence brief — *"Document a POST /api/v1/translations endpoint for a translation API called LinguaAPI. Target audience: frontend engineers."* — the agency produced the following output through the **New API Endpoint** workflow:

---

**POST /api/v1/translations** — Translate Text

Translate a text string from one language to another.

### Request Body

| Name | Type | Required | Default | Description |
|---|---|---|---|---|
| `text` | string | Yes | — | Source text to translate. Max 5000 chars. |
| `source_lang` | string | Yes | — | Source language code (ISO 639-1), e.g. `en`, `ja` |
| `target_lang` | string | Yes | — | Target language code (ISO 639-1), e.g. `es`, `de` |
| `tone` | string | No | `neutral` | Tone: `neutral`, `formal`, or `casual` |

### Example (cURL)

```bash
curl -X POST https://api.linguaapi.com/v1/translations \
  -H "Authorization: Bearer sk-abc123" \
  -H "Content-Type: application/json" \
  -d '{"text": "Hello, how are you?", "source_lang": "en", "target_lang": "es", "tone": "casual"}'
```

### Example Response (200 OK)

```json
{
  "translated_text": "¡Hola! ¿Cómo estás?",
  "source_lang": "en",
  "target_lang": "es",
  "tone": "casual",
  "character_count": 18,
  "credits_used": 1
}
```

### Error Handling

| Status | Scenario |
|---|---|
| 400 | Missing or invalid parameters |
| 401 | Invalid or missing API key |
| 422 | Unsupported language pair |
| 429 | Rate limit exceeded (includes retry header) |

The full output included examples in Node.js, Python, and cURL, a Mermaid sequence diagram, and a quality review report — all produced by routing through the agency pipeline.

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

### Install via companies.sh

```bash
npx companies.sh add Wangxujun0516/docdirector-agency
```

This fetches the latest release tag (currently `v0.1.0`).

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
