# Weekly Pipeline Digest Generator

**Monday pipeline digest in 90 seconds instead of 2 hours.**

## What This Does

Diffs two weekly pipeline snapshots, identifies new deals, stage movements, closures, amount changes, and at-risk deals. Generates executive digest.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, two Salesforce pipeline exports (this week and last week)

## How to Get the Input File

Salesforce: export your pipeline report as CSV every week. Keep a copy. You need this week and last week side by side.

## The Prompt

Copy this into Claude Code:

```
Compare this_week.csv and last_week.csv.

Show me:
- New deals added (with amount)
- Deals that moved forward (stage to stage)
- Deals that moved backward
- Deals that closed (won or lost)
- Deals where amount changed
- Deals with no activity this week over 50K

Generate an executive digest.
Output as weekly_digest.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 2 hours every Monday | 90 seconds |
