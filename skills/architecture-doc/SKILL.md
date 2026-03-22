---
name: architecture-doc
description: Generate an architecture decision record (ADR) or system design doc covering context, options considered, decision, and consequences.
triggers: ["architecture doc", "write an ADR", "architecture decision record", "system design doc", "document this decision"]
---

# Architecture Doc

## What this skill does
Produces a structured Architecture Decision Record (ADR) or system design document from a brief description of the problem space. It captures the context driving the decision, the options that were evaluated, the chosen approach, and the consequences — both positive and negative — of that choice.

## How to invoke
/architecture-doc [decision or system to document]

## Workflow steps

### Step 1 — Gather context
Ask clarifying questions if the trigger message is sparse: What problem are we solving? What constraints apply (team size, latency, cost, existing stack)? What is the scope — single service, cross-cutting concern, or full system?

### Step 2 — Draft the document
Produce a document with the following sections:
- **Title** — short imperative phrase (e.g. "Use Kafka for async event delivery")
- **Status** — Proposed / Accepted / Deprecated / Superseded
- **Context** — background, forces at play, and why a decision is needed now
- **Options considered** — at least two alternatives, each with pros and cons
- **Decision** — the chosen option and the primary rationale
- **Consequences** — what becomes easier, what becomes harder, open risks

### Step 3 — Review and refine
Present the draft and offer to adjust: swap in a different decision, add an option, expand the consequences, or reformat as a Markdown file ready to commit to a `docs/adr/` directory.

## Example outputs
A Markdown document titled "ADR-0012: Adopt event sourcing for the orders domain" with a two-paragraph context section, a comparison table of three options, a clear decision statement, and a bullet list of consequences including a note on operational complexity.

## Live Data Sources
- **CNCF Landscape API** — `landscape.cncf.io` — query the Cloud Native Computing Foundation landscape for current project maturity levels, categories, and adoption data to justify or contextualize technology choices
- **ThoughtWorks Technology Radar** — `thoughtworks.com/radar` — reference the latest Radar blips (Adopt / Trial / Assess / Hold) when comparing options to ground recommendations in industry signal
- **ADR GitHub repo patterns** — search public repositories for `docs/adr/` directories to surface real-world ADR examples and naming conventions that match the team's domain
