---
name: freshness-monitoring
description: Detect stale documentation and prioritize re-generation work.
version: 0.1.0
---

# Freshness Monitoring Skill

## Instructions
Scan the document corpus for staleness indicators and prioritize re-generation.

### Detection Methods
1. **Age-based**: Compare last-updated date against thresholds (30d API, 90d guides, 180d architecture).
2. **Diff-based**: Scan recent commits/diffs for changes to code referenced by docs.
3. **Coverage-based**: Compare documented features against current API surface.

### Process
1. Scan for staleness indicators.
2. Assess each flagged document: full re-write or minor update?
3. Prioritize: public-facing docs and API references above internal docs.
4. Send a prioritized work request to the Director.

### Output
Prioritized list with document path, reason, suggested action, and priority level.
