# Lost Deal Reason Analyzer

**Stop guessing why you lose.**

## What This Does

Reads closed-lost deals CSV, categorizes loss reasons into themes, calculates distribution, identifies patterns by segment/size/stage, and surfaces actionable insights.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, Salesforce closed-lost export as CSV

## How to Get the Input File

Salesforce: Reports tab → Closed Lost Opportunities report (include loss reason, notes, competitor, stage lost at, deal size, segment) → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read closed_lost_q[X].csv.

Categorize all loss reasons into themes:
- Price
- Timing
- Competitor (specify which)
- No Decision / went dark
- Product gap (specify what)
- Other (specify)

Calculate the distribution (% per theme).
Identify patterns by:
- Segment
- Deal size
- Stage lost at

Give me the top 3 actionable insights.

Output as lost_deal_analysis.md with a summary CSV.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A loss reason distribution, pattern analysis by segment/size/stage, and 3 specific actionable insights. Example: 'No Decision kills 31% of deals — your biggest problem isn't competition, it's inaction.'

## How to Verify

Check 10 categorizations for deals you know well. Does the bucketing match your understanding? Are the patterns real or artifacts of bad CRM data?

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Hours of manual analysis | 2 minutes |
