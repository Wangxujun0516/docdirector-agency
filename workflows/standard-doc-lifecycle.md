# Standard Documentation Lifecycle

This workflow defines how a documentation request moves through the agency from entry to delivery.

## Phases

### 1. Intake (Director)

The Director receives a documentation request and determines:
- What type of document is needed (API reference, guide, tutorial, changelog, etc.)
- What skills are required (api-doc-generation, review-and-quality, etc.)
- Which agents to involve
- Priority and timeline

### 2. Research (Researcher)

The Researcher investigates the subject:
- Reads source code, API specs, design docs
- Identifies edge cases and behavioral details
- Produces a structured research brief

### 3. Drafting (Drafter)

The Drafter writes the first full version:
- Follows the style guide
- Incorporates all research brief material
- Produces a complete draft, not an outline

### 4. Review (Reviewer)

The Reviewer evaluates the draft:
- Accuracy, clarity, completeness, style compliance
- Issues rating: approved, minor revisions, major revisions
- If not approved, sends back to Drafter with specific remediation

### 5. Visualization (Visualizer, optional)

If the document benefits from diagrams or charts, the Director routes it through the Visualizer.

### 6. Delivery (Director)

The Director confirms the final output meets quality bar and delivers it to the requester.

### Ongoing Maintenance (Maintainer)

The Maintainer runs on a separate schedule, scanning for staleness and triggering re-generation as needed.

## Diagram

```
                    ┌─────────────┐
                    │   Request   │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │  Director   │
                    │   (Intake)  │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │ Researcher  │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │   Drafter   │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │  Reviewer   │◄──── rejected
                    └──────┬──────┘
                           │ approved
                    ┌──────▼──────┐
                    │ Visualizer  │ (optional)
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │  Director   │
                    │  (Delivery) │
                    └──────┬──────┘
                           │
                    ┌──────▼──────┐
                    │   Output    │
                    └─────────────┘

              ┌──────────────────────────────┐
              │       Maintainer             │
              │  (runs continuously / daily) │
              └──────────────────────────────┘
```
