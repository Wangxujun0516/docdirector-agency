---
name: api-doc-generation
description: Generate API reference documentation from source code, OpenAPI specs, or structured input.
version: 0.1.0
---

# API Doc Generation Skill

## Instructions
Generate or update API reference documentation from structured input.

### Process
1. **Parse** the source or spec to extract endpoints, parameters, request/response shapes, error codes, and authentication.
2. **Organize** into standard sections: overview, authentication, endpoints (grouped by resource), errors, rate limits.
3. **Draft** each endpoint with method, path, parameters, example request, example response.
4. **Include** real-world usage examples for common operations.
5. **Flag** any ambiguities or missing information for the Research Agent.

### Notes
- Prefer automated extraction from structured specs over manual description
- Keep examples realistic — use real parameter values where possible
- Document error responses alongside success responses
