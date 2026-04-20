# PM Superpowers

A Claude Code companion plugin for product managers. Brings disciplined, hard-gated PM workflows to Claude Code — research synthesis, PRD writing, prioritization, and roadmap planning.

## Requirements

- [Claude Code](https://claude.ai/code)
- [superpowers](https://github.com/obra/superpowers) plugin installed

## Installation

```bash
claude plugin marketplace add kvssptj/pm-superpowers
claude plugin install pm-superpowers@pm-superpowers
```

Or for local development:

```bash
claude plugin marketplace add /path/to/pm-superpowers
claude plugin install pm-superpowers@pm-superpowers
```

## Skills

| Skill | Trigger phrases | Output |
|-------|----------------|--------|
| `pm-session-start` | (auto-loads at session start) | — |
| `synthesize-research` | "synthesize research", "user interviews", "make sense of feedback" | `docs/pm/research/` |
| `write-prd` | "write a PRD", "product requirements" | `docs/pm/prd/` |
| `write-brief` | "one-pager", "write a brief" | `docs/pm/briefs/` |
| `prioritize` | "prioritize", "rank features", "RICE", "MoSCoW" | `docs/pm/roadmap/` |
| `roadmap-planning` | "roadmap", "now/next/later", "plan the quarter" | `docs/pm/roadmap/` |

## How It Works

Each skill enforces **hard gates** — you can't jump to the artifact without first locking in the upstream decisions. For a PRD, that means problem statement → target user → success metrics, in that order.

The `pm-session-start` skill loads automatically and routes natural language requests to the right skill. You don't need to know skill names — just describe what you want.

For new initiatives, superpowers' brainstorming skill runs first to explore intent and requirements before any PM artifact is created.

## Artifact Structure

All outputs write to `docs/pm/` in your project:

```
docs/pm/
├── prd/        # Product requirements documents
├── research/   # Research synthesis
├── briefs/     # One-pagers and briefs
└── roadmap/    # Prioritization outputs and roadmaps
```

## Origin

pm-superpowers is the successor to [riff](https://github.com/kvssptj/riff). Where riff was a full multi-agent PM operating system, pm-superpowers is a focused superpowers companion plugin — lighter, installable, and built around hard-gated skill workflows.

## License

MIT
