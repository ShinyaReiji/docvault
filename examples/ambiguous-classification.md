# Ambiguous Classification

This is a non-operational Example Case. It is not a Capture and must not be processed during a Processing Run.

## Input

```md
Capture Date: 2026-05-28

Title: Notes from the planning call

We talked about the inbox workflow, the next write-up, and a possible follow-up with a teammate. There may be a deadline, but I did not write it down.
```

## Expected Judgment

- action: needs-review
- relationship: subcase of `needs-review`
- destination: keep in `inbox/`
- status: `needs-review`
- review_note: state that Note Type classification is ambiguous
- type: do not guess between `project`, `reference`, or `journal`
- body: unchanged
- processing-log: no entry

## Rationale

The Capture is readable, but the Note Type is unclear. It could be tied to an active project, a reusable workflow idea, or a dated personal note, so the agent should not invent a classification.
