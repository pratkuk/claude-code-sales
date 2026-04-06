# MEDDPICC Deal Risk Scorecard

**Evidence-based deal scoring, not gut feel.**

## What This Does

Reads deal artifacts (transcripts, CRM notes, emails) and scores each MEDDPICC criterion with evidence, confidence levels, risk flags, and suggested actions.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, deal artifacts: call transcripts + CRM notes + email threads (any combination)

## How to Get the Input File

Gather everything for the deal into one folder: Gong transcripts (download per call), CRM notes (copy-paste from Salesforce), email threads (copy-paste from Gmail). Drop all in /deals/[account]/.

## The Prompt

Copy this into Claude Code:

```
Read all files in /deals/[account-name]/.

Score this deal against the MEDDPICC framework.

For each criterion (Metrics, Economic Buyer, Decision Criteria, Decision Process, Paper Process, Identify Pain, Champion):
- Evidence found (with specific quotes from sources)
- Confidence level (1-10)
- Risk flag (if confidence < 5)
- Suggested next action

Give me:
- Overall deal health rating (1-10)
- Top 3 risks
- Recommended immediate actions

Output as deal_scorecard.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A MEDDPICC scorecard with evidence-backed scoring per criterion, confidence levels, an overall deal health rating, top 3 risks, and specific next actions.

## How to Verify

Does the evidence actually exist in your materials? Is the confidence score fair? Do the risk flags match your gut? Run this before every deal review.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 45 min of manual assessment | 2 minutes + review |
