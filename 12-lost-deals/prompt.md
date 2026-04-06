# Lost Deal Reason Analyzer — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read closed_lost_q[X].csv.

Categorize all loss reasons into themes:
- Price
- Timing
- Competitor (specify which)
- No Decision / went dark
- Product gap (specify what)
- Other (specify)

Calculate the distribution (% per theme).
Identify patterns by:
- Segment
- Deal size
- Stage lost at

Give me the top 3 actionable insights.

Output as lost_deal_analysis.md with a summary CSV.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
