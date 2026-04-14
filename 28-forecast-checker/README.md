# Forecast Sanity Checker

**Cross-reference forecast vs actual deal signals.**

## What This Does

Reads forecast export, cross-references with activity logs and transcripts for commit deals, scores signal strength, flags mismatches.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, Salesforce forecast export + activity logs + transcripts for commit deals

## How to Get the Input File

Salesforce: export forecast report (commit/best case/pipeline). Also export activity logs for those deals. Download transcripts for commit deals from Gong.

## The Prompt

Copy this into Claude Code:

```
Read forecast.csv.

For each commit deal, cross-reference with activity logs and transcripts.
Score deal signals:
- Recent activity (last 7/14/30 days)
- Stakeholder engagement
- Next steps quality
- Timeline alignment

Flag deals where forecast category does not match signals.
For each flag: explain why, recommend upgrade/downgrade/validate.

Output as forecast_audit.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Gut feel / hope | 3 minutes |
