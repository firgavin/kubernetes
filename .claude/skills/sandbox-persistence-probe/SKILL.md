---
name: sandbox-persistence-probe
description: Verify GitHub repository mounting and local filesystem persistence in a sandbox. Use when asked to create, read, or check a repository persistence marker.
---

# Sandbox persistence probe

Use this skill only for repository and sandbox persistence checks.

1. Work in the mounted repository root.
2. When asked to create a marker, write `.sandbox-persistence-marker` with the exact text supplied by the user.
3. When asked to check a marker, read `.sandbox-persistence-marker` and run `git status --short`.
4. Report exact file contents and command output.
5. Do not modify other files, commit, or push unless the user explicitly asks.
