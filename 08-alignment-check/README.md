# Champion vs Economic Buyer Alignment Check

**Find the gap before it kills the deal.**

## What This Does

Reads two transcripts from the same deal (champion call + EB call), maps what each stakeholder said across key topics, and flags misalignments with specific evidence.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, 2+ call transcripts from the same deal with different stakeholders

## How to Get the Input File

Gong: download transcript from each call individually. Make sure you have at least one call with the champion and one with the EB or decision maker.

## The Prompt

Copy this into Claude Code:

```
Read both transcripts.

For each stakeholder, map what they said about:
- Priorities
- Objections
- Timeline
- Budget
- Success criteria
- Decision process

Build an alignment matrix: topic x stakeholder.
Flag any misalignments between the two with specific evidence (quotes from transcripts).

Output as alignment_check.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

An alignment matrix showing what each stakeholder said on each topic, with misalignments highlighted and supported by specific quotes from the transcripts.

## How to Verify

Read the flagged misalignments. Go back to the transcript context. Does the misalignment hold when you read the full surrounding conversation? If yes, you know what to fix.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Manual / often missed entirely | 90 seconds |
