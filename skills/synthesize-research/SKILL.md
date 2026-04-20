---
name: synthesize-research
description: Synthesize raw research material (interview notes, survey data, support tickets, feedback) into structured insights with evidence. Hard-gated: will not produce insights until themes are identified and agreed upon.
---

# Synthesize Research

Turn raw research material into structured, evidence-backed insights.

<HARD-GATE>
Do NOT write insights or recommendations until:
1. Raw material has been provided
2. Themes have been identified and confirmed by the user
3. Each insight has at least one piece of cited evidence
</HARD-GATE>

## Process

### Gate 1: Collect raw material

Ask the user to provide the raw material. Do not proceed until it is provided. Accept any of:
- Interview notes or transcripts
- Survey responses
- Support ticket excerpts
- User feedback (reviews, NPS comments, etc.)
- Analytics data with context

If nothing is provided, respond: "Please share the raw research material first — interview notes, survey data, support tickets, or any other feedback you want to synthesize."

### Gate 2: Identify themes

Read all the material and identify 3-7 recurring themes. Present them as a numbered list.

Example format:
```
I found these themes across the material:

1. **Onboarding friction** — users struggle to complete setup
2. **Missing notifications** — users miss important updates
3. **Slow search** — search is too slow for power users
4. **Unclear pricing** — users confused about plan limits

Do these themes look right? Any I'm missing or should merge?
```

Do NOT proceed until the user confirms or adjusts the themes.

### Gate 3: Write insights with evidence

For each confirmed theme, write one insight using this format:

```
**[Theme name]**
[One sentence stating the insight — what is true, not what to do about it]
Evidence: [N of M sources] — "[direct quote or paraphrase]", "[another quote]"
```

Example:
```
**Onboarding friction**
New users abandon setup before completing their first project.
Evidence: 4 of 6 interviews — "I gave up after the third screen", "couldn't figure out what to do after signing up"
```

### Output

After insights are confirmed, write the synthesis doc:

```markdown
# Research Synthesis: [Topic]

**Date:** YYYY-MM-DD
**Sources:** [N interviews / N survey responses / etc.]

## Key Insights

[Insights with evidence, one per theme]

## Raw Themes

[Numbered list of themes]

## Open Questions

[Anything the research didn't answer that warrants follow-up]
```

Save to: `docs/pm/research/YYYY-MM-DD-[topic]-synthesis.md`

Replace `[topic]` with a 2-4 word slug (e.g., `onboarding-friction`, `search-usability`).
