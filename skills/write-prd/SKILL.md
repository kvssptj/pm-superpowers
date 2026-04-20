---
name: write-prd
description: Write a product requirements document (PRD). Hard-gated: will not draft the PRD until problem statement, target user, and success metrics are locked in through explicit confirmation.
---

# Write PRD

Produce a well-structured PRD through a disciplined gate process.

<HARD-GATE>
Do NOT write any PRD sections until ALL three gates are passed and confirmed:
1. Problem statement locked
2. Target user defined
3. Success metrics agreed
</HARD-GATE>

## Process

### Gate 1: Lock the problem statement

Ask: "What problem are we solving? Describe it in 2-3 sentences — what's happening today, why it's bad, and who it affects."

When the user responds, reflect it back as a one-sentence problem statement:
```
Problem: [User's problem restated clearly and specifically]
```

Ask: "Does this capture it accurately?"

Do NOT proceed until they confirm.

### Gate 2: Define the target user

Ask: "Who specifically experiences this problem? Describe the user — their role, context, and what they're trying to accomplish when they hit this problem."

Reflect it back:
```
Target user: [Specific user description]
```

Ask: "Is this the right user to optimize for, or are there others?"

Do NOT proceed until they confirm.

### Gate 3: Agree on success metrics

Ask: "How will we know this is solved? What would we measure — and what would 'good' look like for each metric?"

Reflect back:
```
Success metrics:
- [Metric 1]: [target value or direction]
- [Metric 2]: [target value or direction]
```

Ask: "Are these the right metrics? Anything missing?"

Do NOT proceed until they confirm.

### Write the PRD

After all three gates pass, write the full PRD:

```markdown
# PRD: [Feature Name]

**Date:** YYYY-MM-DD
**Status:** Draft
**Author:** [PM name if known, otherwise leave blank]

## Problem

[Confirmed problem statement — 2-4 sentences]

## Target User

[Confirmed target user description]

## Success Metrics

| Metric | Target |
|--------|--------|
| [Metric 1] | [Target] |
| [Metric 2] | [Target] |

## Requirements

### Must Have
- [ ] [Requirement]

### Should Have
- [ ] [Requirement]

### Won't Have (this release)
- [Item explicitly out of scope]

## Open Questions

- [Anything unresolved that needs an answer before build]

## Out of Scope

[Explicit list of what this PRD does NOT cover]
```

Ask the user to fill in requirements together, one section at a time: Must Have first, then Should Have, then explicitly confirm Won't Have items.

Save to: `docs/pm/prd/YYYY-MM-DD-[feature]-prd.md`

Replace `[feature]` with a 2-4 word slug (e.g., `search-redesign`, `onboarding-v2`).
