# Account Research One-Pager

**From zero context to call-ready in 90 seconds.**

## What This Does

Takes a company URL and generates a structured one-pager: what they do, leadership, funding, recent news, tech stack signals, and tailored discovery questions.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, a company website URL

## How to Get the Input File

Just have the company URL or name ready. No export needed.

## The Prompt

Copy this into Claude Code:

```
Research [company.com].

Give me a one-pager:
- What they do
- Who they sell to
- Leadership team (names + titles)
- Recent news or blog posts
- Funding stage and amount
- Tech stack signals
- 5 discovery questions tailored to their business

Output as a structured markdown file.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A markdown one-pager with sections you can skim in 2 minutes. Company overview, key people, recent activity, and discovery questions that reference their actual business.

## How to Verify

Skim their homepage for 2 minutes. Does the brief match reality? Is the funding info current? Are the discovery questions relevant to this specific call?

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 25 min of frantic Googling | 90 seconds + 2-min skim |
