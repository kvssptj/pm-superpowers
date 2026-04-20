---
name: prioritize
description: Prioritize a list of features, ideas, or initiatives using RICE, MoSCoW, or Impact/Effort. Hard-gated: will not rank items until the list is provided, the framework is chosen, and scoring assumptions are stated explicitly.
---

# Prioritize

Rank a list of items through a structured, assumption-explicit process.

<HARD-GATE>
Do NOT produce a ranking until:
1. The list of items is provided
2. The framework is chosen
3. Scoring assumptions are stated and confirmed
</HARD-GATE>

## Process

### Gate 1: Get the list

Ask: "What are the items you want to prioritize? Share them as a list."

Do not proceed until a list is provided. Minimum 2 items.

### Gate 2: Choose a framework

Present the options:

```
Which framework would you like to use?

A) RICE — Reach × Impact × Confidence ÷ Effort. Good for comparing features with different audiences and effort levels.

B) MoSCoW — Must Have / Should Have / Could Have / Won't Have. Good for release scoping and stakeholder alignment.

C) Impact/Effort — Simple 2×2. Good for quick triage when data is thin.
```

Do not proceed until one is chosen.

### Gate 3: State scoring assumptions

Before scoring, ask the user to state their assumptions for each scoring dimension. This is mandatory — hidden assumptions are the main source of bad prioritization.

**For RICE:**
Ask: "Before we score, let's state our assumptions. For each dimension:
- **Reach:** What's the unit? (users per month? sessions per week?) What counts as 'reached'?
- **Impact:** What scale are we using? (e.g., 1=minimal, 2=low, 3=medium, 4=high, 5=massive)
- **Confidence:** What does 80% confidence mean here? Do we have data, or is it a gut call?
- **Effort:** What's the unit? (person-weeks? t-shirt sizes converted to numbers?)"

**For MoSCoW:**
Ask: "Before we sort, let's define the terms for this specific release:
- **Must Have:** What would make us delay the release if missing?
- **Should Have:** What would we drop if we had to, but prefer not to?
- **Could Have:** What's purely additive?
- **Won't Have:** What are we explicitly deferring?"

**For Impact/Effort:**
Ask: "Let's define the axes:
- **High impact:** What does that mean in this context?
- **High effort:** What's the threshold — a sprint? A quarter?"

Do not proceed until the user states and confirms assumptions.

### Produce the ranking

**RICE output:**

```markdown
## Prioritization: [Topic]

**Framework:** RICE
**Date:** YYYY-MM-DD

### Assumptions
- Reach: [stated assumption]
- Impact scale: [stated scale]
- Confidence: [stated definition]
- Effort unit: [stated unit]

### Rankings

| Item | Reach | Impact | Confidence | Effort | RICE Score |
|------|-------|--------|-----------|--------|-----------|
| [Item A] | [N] | [N] | [N%] | [N] | [Score] |
| [Item B] | [N] | [N] | [N%] | [N] | [Score] |

### Notes
[Any items where the score doesn't tell the full story]
```

**MoSCoW output:**

```markdown
## Prioritization: [Topic]

**Framework:** MoSCoW
**Date:** YYYY-MM-DD

### Assumptions
[Confirmed definitions for this release]

### Must Have
- [Item]

### Should Have
- [Item]

### Could Have
- [Item]

### Won't Have (this release)
- [Item]
```

**Impact/Effort output:**

```markdown
## Prioritization: [Topic]

**Framework:** Impact/Effort
**Date:** YYYY-MM-DD

### Assumptions
[Confirmed axis definitions]

### High Impact / Low Effort — Do First
- [Item]

### High Impact / High Effort — Plan
- [Item]

### Low Impact / Low Effort — Fill-ins
- [Item]

### Low Impact / High Effort — Avoid
- [Item]
```

Save to: `docs/pm/roadmap/YYYY-MM-DD-[topic]-prioritization.md`
