# Website Enrichment Engine

**100 companies enriched from their own websites.**

## What This Does

Fetches each company website, extracts what they do, target market, tech signals, size indicators, recent news. Adds confidence score.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, CSV with company names and website URLs

## How to Get the Input File

Any prospect list with URLs. Can come from CRM, Apollo, or a manual list.

## The Prompt

Copy this into Claude Code:

```
Read prospects.csv (columns: Company, URL).

For each company, fetch their website. Extract:
- What they do (one sentence)
- Who they sell to
- Tech stack signals
- Company size indicators
- Recent news or blog posts
- Enrichment confidence score (HIGH/MED/LOW)

Output as enriched_prospects.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 100 tabs open for hours | 5 minutes |
