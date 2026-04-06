# 10-K Annual Report Executive Brief

**200 pages → 2-page summary in 90 seconds.**

## What This Does

Reads a full 10-K filing and extracts revenue breakdown, growth areas, strategic priorities, risk factors, CEO quotes, and suggests positioning for your product.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, a 10-K PDF downloaded from the company's IR page

## How to Get the Input File

Go to the company's Investor Relations page → Annual Reports / SEC Filings → Download the latest 10-K as PDF.

## The Prompt

Copy this into Claude Code:

```
Read this 10-K filing.

Give me an executive brief:
- Revenue breakdown by segment
- YoY growth areas
- Stated strategic priorities (from CEO letter and MD&A)
- Risk factors relevant to [your product category]
- Key quotes from the CEO letter
- Suggested positioning for our product based on their stated goals

Output as executive_brief.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A 2-page executive summary: revenue numbers, where they're growing, what the CEO says matters, risk factors that create urgency, and a positioning suggestion aligned to their stated priorities.

## How to Verify

Verify 3 specific numbers against the filing. Check that strategic priorities match the CEO letter. Confirm the positioning suggestion makes sense for your product.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 200 pages nobody reads | 90 seconds + verification |
