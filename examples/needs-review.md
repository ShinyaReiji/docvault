# Needs Review

This is a non-operational Example Case. It is not a Capture and must not be processed during a Processing Run.

## Input

```md
Capture Date: 2026-05-28

Title maybe: Renewal thing

Need to handle this soon. It might be from the old import, or maybe from a meeting. Not sure whether this is still active.
```

## Expected Judgment

- action: needs-review
- destination: keep in `inbox/`
- status: `needs-review`
- review_note: add one concise reason that the intent or current relevance is unclear
- body: unchanged
- stage: yes, only if the edited frontmatter contains no sensitive material
- commit: yes, as part of the Processing Run only if no sensitive material is present
- processing-log: no entry

## Rationale

The Capture is not clearly sensitive, but it cannot be safely filed because intent and current relevance are unclear. The agent should make the uncertainty visible instead of guessing.
