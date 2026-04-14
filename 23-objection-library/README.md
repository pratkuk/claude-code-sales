# Objection Response Library Builder

**Document what your best reps actually say when prospects push back.**

## What This Does

Scans transcripts for objection moments, extracts objection + response + outcome, clusters similar objections, ranks responses by effectiveness.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, 30-50 call transcripts from top performers

## How to Get the Input File

Gong: download transcripts from your best reps calls. Focus on discovery and negotiation calls where objections are most common.

## The Prompt

Copy this into Claude Code:

```
Read all transcripts in /top-reps/.

Scan for objection moments — when a prospect pushes back, raises a concern, or expresses doubt.

For each objection:
- The exact objection
- How the rep responded
- Outcome (accepted / pushed back / moved on)

Cluster similar objections together.
For each cluster, rank responses by effectiveness.

Output as objection_library.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Never done properly | 3 minutes |
