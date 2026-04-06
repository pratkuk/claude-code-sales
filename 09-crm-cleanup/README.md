# CRM Company Name Cleanup

**20 seconds for a job everyone puts off for months.**

## What This Does

Reads a CSV column of company names, identifies duplicates and variations, standardizes to canonical names, and flags confidence levels.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, a CSV export of company names from your CRM

## How to Get the Input File

Salesforce/HubSpot: export your Accounts or Companies list as CSV. You only need the company name column.

## The Prompt

Copy this into Claude Code:

```
Read company_names.csv.

Identify duplicates and variations of the same company.
Standardize each to a canonical company name.

Output a mapping CSV with columns:
- original_name
- standardized_name
- confidence (HIGH / MED / LOW)
- is_duplicate_of (canonical name, or blank if unique)

Sort by confidence level.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A mapping CSV where every variation is matched to a canonical name with a confidence score. HIGH = safe to auto-merge. LOW = review manually.

## How to Verify

Review the LOW confidence matches. Is 'AWS' really 'Amazon Web Services' in your context? Is 'Amazon.com' retail or cloud? HIGH confidence matches are safe to auto-merge.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| Never done / 'I'll do it later' | 20 seconds |
