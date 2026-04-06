# Deal Status Extraction

**5 calls, 3 hours → 1 deal brief in 2 minutes.**

## What This Does

Reads multiple call transcripts from the same deal chronologically and produces a structured deal status document with decisions, open items, stakeholder positions, and risk flags.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, call transcripts downloaded from Gong/Fireflies (one per call)

## How to Get the Input File

Gong: call page → Download → Transcript (one at a time). Fireflies: export per meeting. Drop all transcripts into one folder.

## The Prompt

Copy this into Claude Code:

```
Read all transcripts in /deals/[account-name]/ in chronological order.

Give me a deal status document with:
- Key decisions made (with which call they happened on)
- Open questions that haven't been resolved
- Objections raised and whether they were addressed
- Next steps promised by both sides (with dates if mentioned)
- Stakeholder positions and sentiment
- Risk flags

Output as deal_status.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A structured deal brief: timeline of decisions, open items nobody followed up on, objections that were never resolved, next steps that were promised but never scheduled, and a stakeholder map.

## How to Verify

Check against your own memory. If a 'decision' or 'next step' doesn't ring a bell, go back to the transcript and verify. The 80% it nails saves you from the 100% you'd otherwise skip.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 3 hours of re-listening | 2 minutes + quick review |
