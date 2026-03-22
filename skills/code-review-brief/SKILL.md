---
name: code-review-brief
description: Write a code review summary covering what changed, why, risk areas to scrutinize, and a testing checklist.
triggers: ["code review brief", "review summary", "write a review brief", "summarize this PR", "review checklist"]
---

# Code Review Brief

## What this skill does
Produces a structured code review brief from a pull request description, diff, or verbal summary of changes. It surfaces what changed and why, calls out the riskiest areas for reviewers to focus on, and generates a concrete testing checklist so nothing falls through the cracks.

## How to invoke
/code-review-brief [PR description, diff, or summary of changes]

## Workflow steps

### Step 1 — Understand the change
Parse the provided input. If given a diff or file list, identify the affected layers (data model, API, business logic, UI, infra). If the input is a natural-language summary, ask for the PR title and key files changed if they are not present.

### Step 2 — Draft the brief
Produce a document with the following sections:
- **Summary** — one paragraph: what changed, why it was needed, and the intended outcome
- **Key changes** — bullet list of the most significant modifications grouped by layer or concern
- **Risk areas** — ranked list of spots that deserve the closest review attention, with a one-line reason for each (e.g. "Auth middleware — privilege escalation if condition is inverted")
- **Testing checklist** — concrete, checkable items covering happy path, edge cases, regressions, and rollback/feature-flag behaviour where applicable

### Step 3 — Tailor and hand off
Offer to expand any section, add a migration or deploy note, or reformat the brief as a GitHub PR comment ready to paste.

## Example outputs
A brief for a database schema migration PR with a two-sentence summary, five bullet points of key changes, three risk areas flagged (index drop, backfill script, ORM model sync), and a nine-item testing checklist including a rollback verification step.
