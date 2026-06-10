---
name: hallucination-detection
description: Identify unsubstantiated claims, fabricated examples, and unsupported assertions in documentation.
version: 0.1.0
---

# Hallucination Detection Skill

## Instructions
Scan documentation for claims that are not supported by the source material.

### Detection Patterns
- **Uncited claims**: Statements presented as fact without a source reference.
- **Fabricated examples**: Code examples using made-up methods, parameters, or return values.
- **Inferred behavior**: Statements about system behavior that are plausible but not confirmed.
- **Over-generalization**: Claims that apply a specific case to all cases without qualification.

### Process
1. Cross-reference each technical claim against the research brief and source material.
2. For claims without a source match, tag as "unsubstantiated."
3. For claims that are inferred but reasonable, tag as "based on inference — verify."
4. For clearly false claims, tag as "hallucination — needs correction."

### Output
A list of flagged claims with severity and recommended action.
