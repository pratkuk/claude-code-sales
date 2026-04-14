# Demo Script Personalizer

**Same demo, different prospect. Personalized in 90 seconds.**

## What This Does

Reads standard demo script and prospect context, reorders sections for impact, adds prospect-specific talking points, suggests what to skip.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, your standard demo script (markdown), prospect context (discovery notes, company info)

## How to Get the Input File

Have your demo script saved as a markdown file. Gather prospect context from CRM notes or call transcript.

## The Prompt

Copy this into Claude Code:

```
Here is my standard demo script:
[paste or point to demo_script.md]

Here is what I know about this prospect:
[paste context]

Reorder sections for maximum impact with this prospect.
Add prospect-specific talking points per section.
Tell me which sections to skip.
Suggest time allocation for a 30-minute demo.

Output as personalized_demo.md.
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## How to Verify

Spot-check the output against your own knowledge. If something looks off, verify against the source material.

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 30 min per demo | 90 seconds |
