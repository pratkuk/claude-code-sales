# Job Posting Intent Signal Mining — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read all job descriptions in /prospects/jobs/.

For each company, extract:
- Tech stack mentioned in requirements
- Pain signals in the responsibilities section
- Seniority level of the role
- Team size hints

Score each company 1-10 on buying intent for [your product category].
Sort by intent score descending.
For the top 10, suggest an outreach angle based on the specific role they're hiring for.

Output as intent_signals.csv.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
