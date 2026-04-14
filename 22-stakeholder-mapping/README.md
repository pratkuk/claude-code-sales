# Stakeholder Mapping from Transcripts

**Who is the champion, who is the blocker — mapped from what people actually said.**

## What This Does

Reads multiple transcripts from same account, identifies unique stakeholders, maps role, sentiment, priorities, influence, and classifies each with evidence.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, call transcripts from same account (different stakeholders)

## How to Get the Input File

Gong: download transcripts from each call with this account. Drop into one folder.

## The Prompt

Copy this into Claude Code:

```
Read all transcripts in /deals/[account]/.

Identify each unique stakeholder.
For each one, map:
- Role
- Sentiment (positive/neutral/negative)
- Stated priorities
- Influence level
- Classification: Champion / Economic Buyer / Coach / Evaluator / Blocker

Support each classification with specific evidence from transcripts.
Output as stakeholder_map.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Manual / often missed | 2 minutes |
