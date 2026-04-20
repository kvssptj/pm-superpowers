---
name: roadmap-planning
description: Build or update a roadmap organized into Now/Next/Later horizons. Hard-gated: requires a prioritized list first. Invokes the prioritize skill if items haven't been scored yet.
---

# Roadmap Planning

Organize prioritized work into a Now/Next/Later roadmap with explicit trade-off notes.

<HARD-GATE>
Do NOT produce a roadmap until:
1. A prioritized list exists (from the prioritize skill or provided by the user)
2. Horizon definitions are agreed upon
3. Each item has an explicit trade-off or rationale note
</HARD-GATE>

## Process

### Gate 1: Confirm prioritized list exists

Ask: "Do you have a prioritized list already? If yes, share it. If not, let's run prioritization first."

If no list exists: say "Let's prioritize first before building the roadmap." Then invoke the `prioritize` skill.

If a list is provided, confirm it contains at minimum: item names and a relative priority or category. Do not proceed with an unranked list.

### Gate 2: Define the horizons

Ask: "Let's define what Now/Next/Later means for this roadmap:
- **Now:** What's the time window? (e.g., this quarter, next 6 weeks)
- **Next:** What's the window? (e.g., next quarter, next 3-6 months)
- **Later:** Everything beyond that, or specific items explicitly deferred?"

Reflect back the definitions and confirm.

### Gate 3: Place items with trade-off notes

For each item, ask the user to confirm which horizon it belongs in AND state the key trade-off or rationale in one sentence.

Example:
```
Where does "Search redesign" go, and what's the one-sentence rationale for that timing?
```

Work through items in priority order. Do not place all items at once without rationale.

### Write the roadmap

```markdown
# Roadmap: [Area or Team Name]

**Date:** YYYY-MM-DD
**Horizons:** Now = [definition] | Next = [definition] | Later = beyond that

## Now

| Item | Rationale |
|------|-----------|
| [Item] | [One-sentence trade-off or rationale] |

## Next

| Item | Rationale |
|------|-----------|
| [Item] | [One-sentence trade-off or rationale] |

## Later

| Item | Rationale |
|------|-----------|
| [Item] | [One-sentence trade-off or rationale] |

## Explicitly Not On Roadmap

| Item | Reason |
|------|--------|
| [Item] | [Why it's not being planned] |

## Open Questions

- [Anything that could change the roadmap if answered differently]
```

Save to: `docs/pm/roadmap/YYYY-MM-DD-roadmap.md`
