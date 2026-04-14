# Website Enrichment Engine — Prompt

Copy-paste this into Claude Code.

```
Read prospects.csv (columns: Company, URL).

For each company, fetch their website. Extract:
- What they do (one sentence)
- Who they sell to
- Tech stack signals
- Company size indicators
- Recent news or blog posts
- Enrichment confidence score (HIGH/MED/LOW)

Output as enriched_prospects.csv.
```

## Customization

- Adjust criteria to match your sales process
- Change output format if needed (CSV, JSON, markdown)
- Add or remove fields based on what is useful for your workflow
