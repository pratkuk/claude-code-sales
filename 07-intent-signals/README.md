# Job Posting Intent Signal Mining

**The best intent signal in sales is free.**

## What This Does

Reads batch of job descriptions and extracts tech stack, pain signals, seniority, team size hints. Scores companies on buying intent and suggests outreach angles.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, job descriptions copied into text files

## How to Get the Input File

LinkedIn Jobs / Indeed / company careers pages: copy-paste 20-30 job descriptions from target accounts into text files in a folder.

## The Prompt

Copy this into Claude Code:

```
Read all job descriptions in /prospects/jobs/.

For each company, extract:
- Tech stack mentioned in requirements
- Pain signals in the responsibilities section
- Seniority level of the role
- Team size hints

Score each company 1-10 on buying intent for [your product category].
Sort by intent score descending.
For the top 10, suggest an outreach angle based on the specific role they're hiring for.

Output as intent_signals.csv.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A ranked CSV with companies scored by buying intent, signal reasons, and personalized outreach angles based on specific hiring signals.

## How to Verify

Click through to 5 original job postings. Do the extracted signals match what's actually in the JD? If yes, start reaching out.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Ongoing / never done well | 2 minutes |
