# G2 Review Sentiment Analyzer — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read competitor_reviews.txt.

Extract themes:
- What users love (with count)
- Common complaints (with count)
- Feature requests (with count)
- Migration triggers — why they switched from or to this product (with count)

For each theme, pull 1-2 key quotes.
Identify: their top complaints that are our strengths.

Output as sentiment_analysis.md.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
