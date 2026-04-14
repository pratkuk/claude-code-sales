# Contract Redline Summarizer

**40-page redline summarized. Commercial changes highlighted. Boilerplate skipped.**

## What This Does

Reads redlined contract, identifies all changes, categorizes by type, highlights commercial/operational changes with plain-English explanations and suggested responses.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, redlined contract (Word doc with track changes or two versions)

## How to Get the Input File

Download the redlined document from email or DocuSign. If you have the original and the marked-up version, use both.

## The Prompt

Copy this into Claude Code:

```
Read this contract.

Identify all changes. Categorize each by:
- Commercial terms
- Legal risk
- Operational impact
- Standard boilerplate

For commercial and operational changes:
- Explain in plain English what changed
- Why it matters for the deal
- Suggested response

Highlight the 5-10 changes that actually affect the business outcome.
Output as redline_summary.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 2 hours of legal review | 2 minutes |
