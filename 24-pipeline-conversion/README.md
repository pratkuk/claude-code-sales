# Pipeline Stage Conversion Calculator

**Stage-by-stage conversion rates and bottleneck identification.**

## What This Does

Calculates conversion rates between stages, average time in stage, identifies bottlenecks, compares by rep and quarter.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, Salesforce opportunity export with stage history or snapshot data

## How to Get the Input File

Salesforce: Reports tab → Opportunities report with stage, dates, amount, owner → Export as CSV.

## The Prompt

Copy this into Claude Code:

```
Read pipeline_data.csv.

Calculate:
- Conversion rate between each stage
- Average time in each stage
- Bottleneck stage (lowest conversion or longest duration)
- Comparison by rep (if owner column exists)
- Comparison by quarter (if date range allows)

Output as conversion_analysis.md + conversion_data.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Hours with pivot tables | 90 seconds |
