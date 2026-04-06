# ICP Lead Scoring

**Score 500 leads against your ICP in 60 seconds.**

## What This Does

Takes a CSV of leads and scores each one against your ICP definition. Adds a score (1-10), reasoning, and priority tier to every row. Sorts by score so you know exactly who to call first.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- **A CSV of leads** with columns like: Name, Company, Title, Industry, Employee Count, Funding Stage

## How to Get the Input File

Export from your CRM or prospecting tool:
- **Salesforce**: Reports tab → Leads/Contacts report → Export as CSV
- **HubSpot**: Contacts → Select list → Export
- **Apollo**: Saved list → Export as CSV
- **Any spreadsheet**: Save as CSV

## The Prompt

Copy this into Claude Code (edit the ICP definition for your product):

```
Read leads.csv.

Score each lead against this ICP:
- B2B SaaS company
- 50-500 employees
- Series A through Series C funding
- Selling to NA or EU markets
Add columns:
- ICP_Score (1-10)
- Reasoning (one sentence explaining the score)
- Priority_Tier (Tier 1 = 8-10, Tier 2 = 5-7, Tier 3 = 1-4)

Sort by ICP_Score descending.
Output as scored_leads.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A CSV file with your original data plus three new columns:

| Name | Company | Title | ... | ICP_Score | Reasoning | Priority_Tier |
|------|---------|-------|-----|-----------|-----------|---------------|
| Sarah K. | Acme Corp | VP Sales | ... | 9 | Right size (200), right stage (Series B), right function | Tier 1 |
| Mike R. | BigCo | CRO | ... | 3 | Enterprise (5000 emp), wrong segment | Tier 3 |

## How to Verify

1. **Spot-check the top 10** — do these actually look like strong ICP fits?
2. **Spot-check the bottom 10** — are these correctly flagged as poor fit?
3. **Read the reasoning** — does the scoring logic make sense?

If scoring is off, adjust the ICP definition in the prompt and re-run. Takes another 60 seconds.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| ~4 hours of LinkedIn research | 60 seconds + 2-minute review |
