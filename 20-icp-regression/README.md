# ICP Scorecard via Regression

**Stop guessing your ICP. Let historical data tell you what predicts wins.**

## What This Does

Runs logistic regression on win/loss outcome against deal attributes, identifies statistically significant predictors, builds weighted scorecard, tests against holdout set.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, 2 years of closed deals (won + lost) exported from Salesforce as CSV with all available attributes

## How to Get the Input File

Salesforce: Reports tab → All Closed Opportunities (Won + Lost, last 24 months) → Include every attribute: industry, employee count, revenue, funding, source, tech stack, ACV, segment, cycle length → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read deals_history.csv.

Run logistic regression on win/loss outcome against all attributes.
Tell me which attributes are statistically significant predictors.
Build a weighted scorecard from the coefficients.
Test against a 20% holdout set.
Score my current pipeline with the model.

Output three files:
1. icp_scorecard.md — the weighted model explained in plain English
2. scored_deals.csv — every deal re-scored with predicted vs actual
3. model_summary.md — accuracy %, top 5 predictors, surprises
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Never done / outsourced | 3 minutes |
