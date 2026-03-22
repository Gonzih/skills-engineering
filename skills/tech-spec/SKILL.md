---
name: tech-spec
description: Write a technical specification covering goals, non-goals, proposed solution, API design, rollout plan, and open questions.
triggers: ["tech spec", "write a spec", "technical specification", "design doc", "RFC", "write an RFC"]
---

# Tech Spec

## What this skill does
Produces a technical specification from a feature idea, bug mitigation plan, or system change description. It defines what is and is not in scope, proposes a concrete solution with enough detail to start implementation, sketches the API or data model, and surfaces open questions that need resolution before work begins.

## How to invoke
/tech-spec [feature, change, or problem to specify]

## Workflow steps

### Step 1 — Clarify scope
Ask if needed: What is the motivation or user need? Who are the stakeholders? Are there hard constraints (latency, cost, backward compatibility, regulatory)? What is the target ship date or milestone?

### Step 2 — Draft the specification
Produce a document with the following sections:
- **Overview** — one paragraph describing what is being built and why
- **Goals** — bullet list of outcomes the spec must achieve
- **Non-goals** — explicit list of things this spec intentionally does not address
- **Proposed solution** — narrative description of the approach, key components, and how they interact; include a simple ASCII or Mermaid diagram if helpful
- **API / interface design** — endpoints, function signatures, data schemas, or CLI flags as appropriate; use code blocks
- **Rollout plan** — phases, feature flags, migration steps, and rollback strategy
- **Alternatives considered** — brief note on other approaches that were rejected and why
- **Open questions** — numbered list of unresolved decisions with a suggested owner for each

### Step 3 — Iterate
Offer to expand any section, add a security or privacy consideration section, generate a skeleton implementation, or produce a trimmed one-pager version for stakeholder alignment.

## Example outputs
A spec for a rate-limiting feature with a two-paragraph overview, five goals, three non-goals, a solution section describing a token-bucket algorithm backed by Redis, a `POST /api/rate-limit/config` endpoint schema, a three-phase rollout with a feature flag, and four open questions around burst limits, observability, and multi-region behaviour.

## Live Data Sources
- **OpenAPI Specification examples from APIs.guru** — `apis.guru` — browse the world's largest directory of OpenAPI definitions to find real-world schema patterns and endpoint conventions that match the domain being specified
- **RFC search at rfc-editor.org** — `rfc-editor.org/search` — locate relevant IETF RFCs (e.g. RFC 7807 for problem details, RFC 6749 for OAuth) to cite normative standards in protocol or API design sections
- **Stack Overflow Developer Survey data** — `survey.stackoverflow.co` — reference the latest annual survey for technology adoption statistics (languages, frameworks, tools) to justify stack choices or benchmark against industry norms in the Alternatives Considered section
