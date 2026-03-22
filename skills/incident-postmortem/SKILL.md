---
name: incident-postmortem
description: Write a blameless postmortem covering timeline, root cause, contributing factors, and action items with owners.
triggers: ["incident postmortem", "write a postmortem", "blameless postmortem", "post-incident review", "incident report"]
---

# Incident Postmortem

## What this skill does
Produces a blameless postmortem document from an incident summary, chat logs, or verbal description of what happened. It reconstructs the event timeline, identifies the root cause and contributing factors using systems-thinking rather than finger-pointing, and surfaces concrete action items with suggested owners to prevent recurrence.

## How to invoke
/incident-postmortem [incident summary, timeline notes, or description of what happened]

## Workflow steps

### Step 1 — Collect incident data
Extract or ask for: incident start and end times, severity/impact (users affected, revenue, SLA breach), services involved, who responded, and a rough sequence of events. If chat logs or monitoring screenshots are available, use them to anchor the timeline.

### Step 2 — Draft the postmortem
Produce a document with the following sections:
- **Incident summary** — one paragraph: what broke, duration, customer impact, and severity level
- **Timeline** — chronological table of events (UTC timestamps, event description, actor)
- **Root cause** — the deepest systemic cause, stated without blaming individuals
- **Contributing factors** — other conditions that made the incident worse or harder to detect (e.g. lack of alerting, deployment process gap, unclear runbook)
- **What went well** — things the team did right during the response
- **Action items** — table with columns: Action | Owner | Priority | Due date. Minimum: one item addressing root cause, one improving detection, one improving response.

### Step 3 — Review and finalize
Offer to sharpen the root cause statement, add a "lessons learned" narrative section, adjust tone for executive vs. engineering audiences, or export as a Confluence-ready format.

## Example outputs
A postmortem for a 47-minute database failover incident with a six-row timeline, a root cause of "manual failover runbook not tested after infrastructure upgrade," three contributing factors, two "went well" items, and a five-row action items table with owners and due dates.
