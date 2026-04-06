# Competitive Battlecard Generator

**From zero intel to call-ready in 3 minutes.**

## What This Does

Fetches competitor web pages and builds a structured battlecard with positioning, pricing, features, honest strengths/weaknesses, objection handlers, and landmines to set.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, 3-5 competitor URLs (main page, pricing, features)

## How to Get the Input File

Just have the URLs ready. Claude Code fetches the pages directly.

## The Prompt

Copy this into Claude Code:

```
Fetch these URLs:
- [competitor.com]
- [competitor.com/pricing]
- [competitor.com/features]

Build a competitive battlecard:
- What they do (positioning)
- Who they target
- Pricing model and tiers
- Key features (top 5-7)
- Strengths (be honest — where they're actually good)
- Weaknesses (what's missing or limited)
- Our differentiators (where we win head-to-head)
- Objection handlers (when a prospect pushes back)
- Landmines to set early (questions that expose their gaps)

Output as battlecard.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A structured battlecard with honest competitive intel. Strengths based on what's actually on their site, weaknesses based on what's missing, and landmines you can plant early in conversations.

## How to Verify

Verify the pricing — it changes. Check feature claims against your own product knowledge. Make sure the 'strengths' section is honest and the 'weaknesses' are real, not wishful thinking.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 1 hour of browsing | 3 minutes + review |
