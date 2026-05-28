# Normal Processing

This is a non-operational Example Case. It is not a Capture and must not be processed during a Processing Run.

## Input

```md
Capture Date: 2026-05-28

Title: Inbox-first note handling

Putting raw notes into one inbox first reduces the need to decide the final folder at capture time. The filing decision can happen later, when the note is reviewed with more context.
```

## Expected Judgment

- action: file
- destination: `notes/references/`
- type: `reference`
- filename rule: `YYYY-MM-DD-<slug>.md`
- frontmatter: add `title`, `created`, and `type` matching `schema/note.schema.json`
- body: light proofreading only, preserving meaning and voice
- processing-log: append one line

## Rationale

The input contains a durable reusable principle and does not mention a specific active project, personal log, sensitive data, or user instruction to avoid processing.
