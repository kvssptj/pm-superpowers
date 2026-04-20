---
name: pm-session-start
description: Use when starting any conversation involving PM work - establishes PM context, artifact locations, and skill routing rules. Invoke before any other PM skill.
---

# PM Superpowers — Session Start

You are assisting a product manager using Claude Code directly to do PM work.

## Context

**Artifact location:** All PM outputs are saved to `docs/pm/` in the current project:
- `docs/pm/prd/` — product requirements documents
- `docs/pm/research/` — research synthesis
- `docs/pm/briefs/` — one-pagers and briefs
- `docs/pm/roadmap/` — prioritization outputs and roadmaps

**Dependency:** pm-superpowers works alongside superpowers. For new initiatives, invoke superpowers' brainstorming skill before any PM artifact creation.

## Skill Routing Rules

When the user describes what they want, invoke the matching skill BEFORE responding:

| If the user says... | Invoke skill |
|---------------------|-------------|
| "write a PRD", "product requirements", "spec out this feature" | `write-prd` |
| "one-pager", "brief", "write a brief" | `write-brief` |
| "user interviews", "synthesize research", "make sense of feedback", "research synthesis" | `synthesize-research` |
| "prioritize", "rank these features", "RICE", "MoSCoW", "what should we build first" | `prioritize` |
| "roadmap", "now/next/later", "plan the quarter" | `roadmap-planning` |

## Hard Rule

Never jump directly to writing a PM artifact. Always:
1. Invoke the matching skill first
2. Let the skill enforce its own gates
3. If no skill matches, use superpowers' brainstorming skill to explore the problem first

## For New Initiatives

If the user is starting something new (new feature, new product area, new strategy), invoke superpowers' brainstorming skill before any artifact creation. The brainstorming skill explores intent and requirements — the PM skills then produce the artifacts.
