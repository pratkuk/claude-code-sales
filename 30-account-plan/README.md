# Account Plan Builder

**Scattered CRM notes, transcripts, and emails into one coherent account plan.**

## What This Does

Reads mixed deal artifacts from one folder, synthesizes into structured account plan with org map, competitive context, and 90-day action plan.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, all account artifacts dumped into one folder (CRM notes, transcripts, emails, Slack messages)

## How to Get the Input File

Gather everything: copy-paste CRM notes, download Gong transcripts, copy-paste email threads and Slack messages. Dump all into one folder. Do not organize.

## The Prompt

Copy this into Claude Code:

```
Read all files in /accounts/[name]/.

Synthesize into a structured account plan:
- Org map (who is involved, their roles)
- Current state of the relationship
- Their stated goals and pain points
- Competitive landscape
- Our positioning and progress
- 90-day action plan with specific next steps

Output as account_plan.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Half a day | 3 minutes |
