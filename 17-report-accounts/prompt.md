# Analyst Report → Target Account List — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read this PDF report.

Extract every company mentioned.
For each company:
- Company name
- Segment they're in
- Report positioning (leader / challenger / niche / emerging)
- Page reference
- Suggested outreach angle based on their position

Output as target_accounts.csv.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
