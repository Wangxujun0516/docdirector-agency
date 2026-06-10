---
name: doc-research
description: Structured methodology for investigating source code, APIs, and specifications to produce accurate documentation.
version: 0.1.0
---

# Doc-Research Skill

## Instructions
Perform structured research on code, APIs, or systems to produce a reliable brief for downstream documentation agents.

### Step 1: Source Identification
- Identify all relevant sources: code files, API specs, changelogs, design docs, support tickets.
- Prioritize official / canonical sources over community or inferred sources.

### Step 2: Fact Extraction
- Extract parameters, return values, types, defaults, and constraints for each API or function.
- Document error conditions: what can fail, how it fails, what the caller sees.
- Note deprecations, version differences, and behavioral quirks.

### Step 3: Example Gathering
- Collect at least one realistic usage example per endpoint or function.
- Include one edge case or failure example.
- Verify examples against the actual code — never fabricate.

### Step 4: Output
A research brief in Markdown with source citations.
