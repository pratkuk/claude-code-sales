# Analyst Report → Target Account List

**40 pages → a ready-to-dial prospect list in 2 minutes.**

## What This Does

Reads an analyst report PDF, extracts every company mentioned, categorizes by segment and positioning, adds page references, and suggests outreach angles.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, an analyst report PDF (Gartner, Forrester, or similar)

## How to Get the Input File

Download the PDF from the analyst firm's website or your subscription portal.

## The Prompt

Copy this into Claude Code:

```
Read this PDF report.

Extract every company mentioned.
For each company:
- Company name
- Segment they're in
- Report positioning (leader / challenger / niche / emerging)
- Page reference
- Suggested outreach angle based on their position

Output as target_accounts.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A CSV with every company from the report, categorized by segment and positioning, with page references and a suggested outreach angle for each.

## How to Verify

Cross-check 10 companies against the PDF. Are the page references accurate? Does the segment classification match? Is the positioning tag correct?

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 2 hours reading a report nobody finishes | 2 minutes + cross-check |
