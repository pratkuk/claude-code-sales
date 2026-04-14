# Competitive Mention Tracker

**Track which competitors come up across 50 transcripts, how often, and how reps handle it.**

## What This Does

Reads batch of call transcripts, scans for competitor mentions, extracts context and rep responses, groups by competitor with frequency and win/loss correlation.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, 30-50 call transcripts in a folder

## How to Get the Input File

Gong: download transcript per call. Batch into one folder.

## The Prompt

Copy this into Claude Code:

```
Read all transcripts in /calls/.

Scan for competitor mentions. For each mention extract:
- Which competitor
- What was said
- Who said it (prospect or rep)
- Context of the conversation
- How the rep handled it
- Outcome of that segment

Group by competitor.
Show frequency and common objections per competitor.
Output as competitive_intel.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 3 hours of manual listening | 3 minutes |
