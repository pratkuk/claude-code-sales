# Proposal Comparison Analyzer

**Your proposal vs theirs. Side by side in 2 minutes.**

## What This Does

Compares two proposals across pricing, features, SLAs, implementation, support. Identifies advantages per dimension and suggests talking points.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, your proposal PDF/markdown + competitor proposal or detailed notes

## How to Get the Input File

Have both proposals. If you do not have the competitor proposal, compile notes from what the prospect told you about their offer.

## The Prompt

Copy this into Claude Code:

```
Compare these two proposals.

Build a comparison matrix across:
- Pricing structure
- Included features
- SLAs
- Implementation timeline
- Support terms
- Unique differentiators

For each dimension: who has the advantage and why.
Suggest talking points for dimensions where we are weaker.

Output as comparison_matrix.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 1 hour | 2 minutes |
