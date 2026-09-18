# Template: Conference Talk Submission

Every talk in this repo follows the structure below. File location and naming:
`<year>/<topic-slug>.md` (e.g. `2027/agentic-sdlc-platform.md`).

## Structure

```markdown
# <Talk Title>

## Elevator Pitch
## Abstract
## Full Description
## What the Audience Will Gain
## Target Audience
## Level
## Suggested Duration
## Tags
```

## Field guidance

### Elevator Pitch (≤ 200 words)

The program-listing blurb and the text for short CFP forms. It must hook the
reader in the first sentence and work with zero context. Write it last.

### Abstract (≤ 500 words)

The standard CFP submission text. Self-contained: the problem, the approach,
what the audience will see, and why it matters now. Reviewers often read only
this — never assume they also saw the pitch or the full description.

### Full Description (no limit)

The master copy and source of truth. Everything the talk covers, lightly
structured, including the takeaway list. The Elevator Pitch and Abstract are
*derived* from this section, not the other way around.

### What the Audience Will Gain

Bulleted, concrete, and phrased as outcomes ("how to…", "why…"), not topic
names. 4–7 bullets.

### Target Audience

Job titles and situations, not just "developers".

### Level

One of: Beginner / Intermediate / Advanced (or a combination, with a note on
what prior knowledge is assumed).

### Suggested Duration

Typical formats: 25–40 min talk, optional live demo note.

### Tags

Comma-separated, lowercase, 4–7 tags matching the conference tracks you're
targeting.

## Word-count rule

| Tier | Section | Cap |
|------|---------|-----|
| 1 | Elevator Pitch | ≤ 200 words |
| 2 | Abstract | ≤ 500 words |
| 3 | Full Description | none |

Key rule: **each of the three descriptions must stand alone.** A reviewer or
program committee may only ever see one of them. Derive tiers 1 and 2 from
tier 3, and verify the caps by extracting the section and running `wc -w`
before submitting.
