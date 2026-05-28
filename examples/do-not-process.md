# Do Not Process

This is a non-operational Example Case. It is not a Capture and must not be processed during a Processing Run.

## Input

```md
---
do-not-process: true
---

Private scratchpad for later. Do not touch this yet.
```

## Expected Judgment

- action: do-not-process
- destination: keep in `inbox/`
- body: unchanged
- frontmatter: unchanged
- move: no
- stage: no
- commit: no
- processing-log: no entry

## Rationale

The frontmatter contains a parseable user instruction. The agent is not being asked to judge the content, so the whole file must be left untouched.
