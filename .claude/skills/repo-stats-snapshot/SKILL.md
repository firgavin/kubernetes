---
name: repo-stats-snapshot
description: Generate a quick read-only snapshot of repository statistics (file counts by type, total lines, recent commit count). Use when asked for a repo stats report, codebase overview, or file/line count summary.
---

# Repo stats snapshot

Use this skill only for producing a quick, read-only overview of a repository's size and activity.

1. Work in the mounted repository root; do not modify any files.
2. Count files grouped by extension, e.g. `git ls-files | sed 's/.*\.//' | sort | uniq -c | sort -rn`.
3. Count total lines of tracked text files, e.g. `git ls-files | xargs wc -l | tail -1`.
4. Count commits in a recent window if asked, e.g. `git log --since="30 days ago" --oneline | wc -l`.
5. Report the numbers in a short table or list; do not interpret or embellish beyond the raw counts.
6. Do not commit or push unless the user explicitly asks.
