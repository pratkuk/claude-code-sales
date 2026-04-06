# Win/Loss Analysis Report — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read q[X]_opportunities.csv.

Analyze:
- Win patterns (what's common across won deals)
- Loss patterns (what's common across lost deals)
- Competitor-specific win rates
- Segment performance (win rate by segment)
- Sales cycle length vs outcome correlation

Give me:
- Executive summary (5 sentences)
- Win patterns vs loss patterns (side by side)
- Top 5 actionable recommendations

Output as win_loss_analysis.md.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
