# Deal Status Extraction — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read all transcripts in /deals/[account-name]/ in chronological order.

Give me a deal status document with:
- Key decisions made (with which call they happened on)
- Open questions that haven't been resolved
- Objections raised and whether they were addressed
- Next steps promised by both sides (with dates if mentioned)
- Stakeholder positions and sentiment
- Risk flags

Output as deal_status.md.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
