---
description: (Opus 4.5) Generate a git commit message for staged changes
---

## Context

- Current git status: !`git status`
- Staged changes diff: !`git diff --staged`
- Current branch: !`git branch --show-current`
- Recent commits: !`git log --oneline -10 2>/dev/null || echo "No commits yet"`

## Your task

If the staged diff is empty, output: No staged changes. Stage changes first.

Otherwise, output only the commit message (no preamble, no explanation). Follow the style of recent commits, or use conventional commits if there are no commits yet.

Do not use any tools or do anything else.
