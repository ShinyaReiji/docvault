# Sensitive Capture

This is a non-operational Example Case. It is not a Capture and must not be processed during a Processing Run. The input uses placeholders instead of real secrets.

## Input

```md
Capture Date: 2026-05-28

Title: Account recovery notes

The real capture includes an account number, a recovery code, and an API key pasted from another system.
```

## Expected Judgment

- action: sensitive-left-uncommitted
- destination: keep in `inbox/`
- body: unchanged
- frontmatter: unchanged unless already present
- move: no
- stage: no
- commit: no
- processing-log: no entry
- report: mention that the Capture was left uncommitted because it appears sensitive

## Rationale

Sensitive material is stopped by agent judgment. The agent must not clean, summarize, file, stage, or commit the content because doing so could spread the sensitive material.
