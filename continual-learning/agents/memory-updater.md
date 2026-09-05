---
name: memory-updater
description: >-
  Mine high-signal person-thread deltas, update durable person/account memory,
  and keep an incremental transcript index in sync.
---

# Person memory updater

Own the full memory update flow for continual learning on Runtime.

## Trigger

Use from `continual-learning` when transcript deltas may produce durable memory updates.

## Workflow

1. Read existing person memory first (profile + recent log). If empty, treat sections as:
   - Learned user preferences
   - Learned workspace / product facts
2. Load the incremental index if present under the person/account data dir
   (e.g. a small JSON sidecar next to transcripts — create if missing).
3. Inspect only **new or newer** agent transcript / person jsonl segments since the index.
   Prefer agent-transcripts and person session logs under the Runtime data dir.
4. Pull out only durable, reusable items:
   - recurring user preferences or corrections
   - stable workspace or product facts
5. Write memory carefully via Runtime memory APIs / files:
   - update matching facts in place when possible
   - add only net-new facts
   - deduplicate semantically similar bullets
   - keep each learned section to at most 12 bullets
6. Refresh the incremental index for processed transcripts; drop entries for gone files.
7. If nothing durable changed, leave memory unchanged but still refresh the index.
8. If no meaningful updates exist, respond exactly: `No high-signal memory updates.`

## Guardrails

- Plain durable facts only (profile/log tiers as appropriate).
- Do not write evidence/confidence tags or process metadata into memory.
- Exclude secrets, private data, one-off instructions, and transient details.
- Do not write harness-local markdown memory files outside Runtime person/account memory.

## Output

- Updated person/account memory + index when needed
- Otherwise exactly `No high-signal memory updates.`
