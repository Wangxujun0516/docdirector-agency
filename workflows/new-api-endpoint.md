---
name: New API Endpoint Documentation
description: End-to-end workflow for documenting a new API endpoint.
version: 0.1.0
---

# New API Endpoint Documentation Workflow

**Trigger**: Human Director provides endpoint spec, code, or PR link.

## Step 1: Director Orchestration
Documentation Director receives brief and delegates.

## Step 2: Research Agent
- Use `doc-research` skill to gather context from codebase, tickets, related endpoints.
- Identify target audience and existing patterns.

## Step 3: Outlining & Structuring Agent
- Create logical structure (Overview, Authentication, Parameters, Examples, Error Handling, etc.).

## Step 4: Drafting Agent + Code Sample Agent
- Generate core content.
- Use `api-doc-generation` and code sample skills to produce tested examples (Node.js, Python, cURL).

## Step 5: Diagram & Visualization Agent
- Generate Mermaid sequence diagrams or architecture flow using `mermaid-diagram-generation`.

## Step 6: Review & Quality Agent
- Run full `review-and-quality`, `hallucination-detection`, `style-guide-enforcement`, and `user-empathy-mapping` skills.
- Flag issues and suggest fixes.

## Step 7: Human Director Review
- Human reviews, provides feedback, iterates as needed.

## Step 8: Maintenance Setup
- Register with Maintenance Agent for future freshness monitoring.

## Output
- Markdown/MDX file ready for Git commit.
- Review summary and change log.

**Success Criteria**: Accurate, empathetic, complete, and ready for publication.
