# Stale Deal Detector — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read pipeline.csv.

Flag every deal where:
- Last activity is more than 14 days ago
- Stuck in the same stage for 30+ days
- Amount over $50K with no next step logged

Sort by risk level (highest risk first).
For each flagged deal, suggest a specific action.

Output as stale_deals_report.md.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
