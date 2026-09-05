---
name: continual-learning
description: >-
  Orchestrate continual learning by delegating transcript mining and person
  memory updates to the memory-updater agent brief.
disable-model-invocation: true
---

# Continual learning

Keep person memory current by delegating the update flow to one worker.

## Trigger

Use when the user asks to mine prior chats, refresh durable memory, or run the continual-learning loop.

## Workflow

1. Hand off to the `memory-updater` agent brief (same plugin `agents/`).
2. Return the updater result.

## Guardrails

- Keep this skill orchestration-only.
- Do not mine transcripts or write memory in the parent flow.
- Do not bypass the memory-updater brief.
- Use Runtime person/account memory and agent transcript paths only.
