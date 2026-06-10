---
name: review-and-quality
description: Rigorous multi-pass review process for technical documentation.
version: 0.1.0
---

# Review & Quality Skill

## Instructions
Perform a structured, multi-pass review on any documentation draft.

### Pass 1: Accuracy & Hallucination Check
- Verify all technical claims against provided sources/code.
- Flag any unsubstantiated statements.
- Require citations or "based on inference" labels.

### Pass 2: Clarity & Structure
- Is the information architecture logical?
- Active voice? Short sentences where possible?
- Proper headings, lists, code blocks?

### Pass 3: Audience Empathy & Tone
- Does it speak to the intended persona?
- Helpful, professional, never condescending.

### Pass 4: Completeness
- Missing edge cases? Failure modes? Monitoring tips? Examples?

### Output
```markdown
## Review Summary

**Strengths:**
...

**Issues:**
- Critical: ...
- Major: ...
- Suggestions: ...

**Recommended Changes:**
...

**Overall Score:** /10
**Ready for Human Review:** Yes/No
```

Use this skill before any content is considered final.
