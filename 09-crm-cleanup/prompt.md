# CRM Company Name Cleanup — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read company_names.csv.

Identify duplicates and variations of the same company.
Standardize each to a canonical company name.

Output a mapping CSV with columns:
- original_name
- standardized_name
- confidence (HIGH / MED / LOW)
- is_duplicate_of (canonical name, or blank if unique)

Sort by confidence level.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
