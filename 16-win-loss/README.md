# Win/Loss Analysis Report

**A quarter of insights in 3 minutes.**

## What This Does

Analyzes all closed deals (won + lost) for patterns: win patterns, loss patterns, competitor win rates, segment performance, cycle length correlations, and recommendations.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, quarterly opportunity export from Salesforce as CSV

## How to Get the Input File

Salesforce: Reports tab → All Opportunities (Closed Won + Closed Lost) for the quarter → Include: amount, stage, competitor, segment, cycle length, source, loss reason, notes → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read q[X]_opportunities.csv.

Analyze:
- Win patterns (what's common across won deals)
- Loss patterns (what's common across lost deals)
- Competitor-specific win rates
- Segment performance (win rate by segment)
- Sales cycle length vs outcome correlation

Give me:
- Executive summary (5 sentences)
- Win patterns vs loss patterns (side by side)
- Top 5 actionable recommendations

Output as win_loss_analysis.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A full win/loss report with executive summary, pattern analysis, competitor win rates, segment breakdown, and 5 specific recommendations you can present at your QBR.

## How to Verify

Check the win rates against your CRM dashboards. Do the patterns match your intuition? Flag the surprises — then investigate.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| A full day of manual analysis | 3 minutes |
