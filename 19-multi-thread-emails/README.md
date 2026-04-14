# Multi-Threading Email Sequence Builder

**4 stakeholders, 4 personalized emails, one consistent narrative.**

## What This Does

Takes account context and stakeholder details, generates role-specific email drafts with different value prop angles while maintaining narrative consistency.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, account context (company info, deal stage, stakeholder roles and what you know about each)

## How to Get the Input File

CRM notes + call transcripts + LinkedIn profiles. Compile what you know about each stakeholder.

## The Prompt

Copy this into Claude Code:

```
Here are 4 stakeholders at [account]:

[For each: name, role, what they care about, what you have discussed]

Draft a personalized email for each.
Different value prop angle per role.
Keep the core narrative consistent — no contradictions.
Include role-specific subject lines and CTAs.

Output as stakeholder_emails.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 1-2 hours | 2 minutes |
