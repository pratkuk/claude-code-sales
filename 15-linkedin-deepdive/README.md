# LinkedIn Prospect Deep Dive

**Career arc, interests, and 3 conversation starters in 60 seconds.**

## What This Does

Analyzes a LinkedIn profile to identify career trajectory patterns, themes, interests, and generates tailored conversation starters and potential pain points.

## What You Need

- **Claude Code** installed ([guide](https://docs.anthropic.com/en/docs/claude-code))
- Claude Code installed, a LinkedIn profile (copy-pasted as text)

## How to Get the Input File

Go to the person's LinkedIn profile. Select all text on the page. Copy-paste into a text file or directly into Claude Code.

## The Prompt

Copy this into Claude Code:

```
Here's a LinkedIn profile (pasted below).

Give me:
- Career trajectory summary (not just job titles — the pattern)
- Themes across role changes
- Interests and topics they post/comment about
- 3 conversation starters tailored to their background
- Potential pain points based on their current role

[paste LinkedIn profile text here]
```

See [prompt.md](./prompt.md) for the copy-pasteable version.

## What You'll Get Back

A prospect brief with career arc patterns, themes, interests, 3 tailored conversation starters that feel natural (not researched), and potential pain points based on their current role.

## How to Verify

Skim their LinkedIn profile for 2 minutes. Do the conversation starters feel natural? Is the career arc accurate? Would you actually say these things on a call?

## Time Saved

| Manual | Claude Code |
|--------|-------------|
| 20 min of LinkedIn scrolling | 60 seconds + 2-min skim |
