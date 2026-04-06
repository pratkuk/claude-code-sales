# Personalized First Lines at Scale

**30 prospects, 30 openers. Not generic.**

## What This Does

Takes a CSV of prospects, researches each one (via provided URLs or web fetch), generates 2-3 personalized first line options per prospect with source attribution.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, a CSV of prospects with name, company, title, and optionally a LinkedIn URL or notes

## How to Get the Input File

Prepare a CSV with columns: Name, Company, Title, URL (optional), Notes (optional). Can come from any CRM, prospecting tool, or manual list.

## The Prompt

Copy this into Claude Code:

```
Read prospects.csv (columns: Name, Company, Title, URL, Notes).

For each prospect:
- Research their company (fetch URL if provided)
- Generate 2-3 personalized first line options
- Each must reference a specific, verifiable detail about the person or company
- Add a source_of_personalization column so I can verify

Output as personalized_lines.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

An updated CSV with 2-3 first line options per prospect, each referencing something specific and verifiable, with a source column you can check.

## How to Verify

Read 5 first lines. Click through to the source. Are the personal details accurate? Would you actually send this? Delete the bad ones, send the good ones.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 3-5 hours of manual research | 5 minutes + review |
