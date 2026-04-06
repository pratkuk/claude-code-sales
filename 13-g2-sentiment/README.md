# G2 Review Sentiment Analyzer

**200 reviews synthesized in 90 seconds.**

## What This Does

Reads copy-pasted competitor reviews, extracts themes (love, hate, feature requests, migration triggers), quantifies by count, and surfaces opportunities.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, competitor reviews copied into a text file

## How to Get the Input File

Go to competitor's G2/Capterra/TrustRadius page. Copy-paste 50-100 reviews into a text file (competitor_reviews.txt).

## The Prompt

Copy this into Claude Code:

```
Read competitor_reviews.txt.

Extract themes:
- What users love (with count)
- Common complaints (with count)
- Feature requests (with count)
- Migration triggers — why they switched from or to this product (with count)

For each theme, pull 1-2 key quotes.
Identify: their top complaints that are our strengths.

Output as sentiment_analysis.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A sentiment report with themes quantified by count, key quotes per theme, and a highlighted section showing where their weaknesses are your strengths.

## How to Verify

Read 5 original reviews. Does the thematic analysis hold up? Are the key quotes pulled in context? Does the 'opportunity' section match your actual product strengths?

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Hours of reading reviews | 90 seconds |
