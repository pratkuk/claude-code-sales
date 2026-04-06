# Stale Deal Detector

**Find every dead deal in your pipeline in 30 seconds.**

## What This Does

Reads a pipeline CSV and flags deals with no activity, stuck stages, or high-value deals with no next step. Sorts by risk level and suggests specific actions.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, Salesforce pipeline export as CSV

## How to Get the Input File

Salesforce: Reports tab → Opportunities report (include last activity date, stage, amount, owner, next step) → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read pipeline.csv.

Flag every deal where:
- Last activity is more than 14 days ago
- Stuck in the same stage for 30+ days
- Amount over $50K with no next step logged

Sort by risk level (highest risk first).
For each flagged deal, suggest a specific action.

Output as stale_deals_report.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

An alert report with every stale deal sorted by risk, the reason it was flagged, and a suggested next action for each.

## How to Verify

Cross-check 5 flagged deals in Salesforce. Is the last activity date accurate? Are the flags fair? If yes, trust the rest.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 45 min every Monday | 30 seconds |
