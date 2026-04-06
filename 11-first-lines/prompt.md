# Personalized First Lines at Scale — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read prospects.csv (columns: Name, Company, Title, URL, Notes).

For each prospect:
- Research their company (fetch URL if provided)
- Generate 2-3 personalized first line options
- Each must reference a specific, verifiable detail about the person or company
- Add a source_of_personalization column so I can verify

Output as personalized_lines.csv.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
