# Territory Segmentation

**New territory, 2000 accounts, segmented and prioritized in one session.**

## What This Does

Reads territory account list, segments into tiers based on ICP criteria, calculates territory potential, produces prioritized target list.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, territory account list exported from Salesforce as CSV

## How to Get the Input File

Salesforce: Reports tab → Territory Accounts report → Include company, industry, size, revenue, location, existing relationship → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read territory_accounts.csv.

Segment into Tier 1 (top priority), Tier 2 (medium), Tier 3 (low) based on this ICP criteria:
[paste your criteria or reference ICP scorecard weights]

Calculate territory potential by tier.
Give me the top 50 accounts to focus on first with reasoning.

Output as territory_plan.csv + territory_summary.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Several hours | 2 minutes |
