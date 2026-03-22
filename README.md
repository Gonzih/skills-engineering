# @gonzih/skills-engineering

Claude Code skill suite for software engineers, tech leads, and engineering managers.

## Skills

| Skill | Invoke | What it does |
|-------|--------|--------------|
| `architecture-doc` | `/architecture-doc` | Generate an ADR or system design doc |
| `code-review-brief` | `/code-review-brief` | Write a structured code review summary |
| `incident-postmortem` | `/incident-postmortem` | Write a blameless postmortem |
| `tech-spec` | `/tech-spec` | Write a technical specification |

## Install

```bash
npx @gonzih/skills-engineering
```

Then restart Claude Code.

## Usage

### `/architecture-doc`
```
/architecture-doc We need to decide between a monorepo and polyrepo for our new platform.
```
Produces an ADR with context, options considered, decision, and consequences.

### `/code-review-brief`
```
/code-review-brief [paste PR description or diff]
```
Produces a review summary with key changes, risk areas, and a testing checklist.

### `/incident-postmortem`
```
/incident-postmortem Database went down at 14:32 UTC, came back at 15:19 UTC. Root cause was a bad deploy.
```
Produces a blameless postmortem with timeline, root cause, contributing factors, and action items.

### `/tech-spec`
```
/tech-spec Rate limiting on our public API — need per-user and per-IP limits.
```
Produces a spec with goals, non-goals, proposed solution, API design, rollout plan, and open questions.

## License

MIT
