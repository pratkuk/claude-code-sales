# MEDDPICC Deal Risk Scorecard — Prompt

Copy-paste this into Claude Code. Edit the bracketed sections for your specific use case.

```
Read all files in /deals/[account-name]/.

Score this deal against the MEDDPICC framework.

For each criterion (Metrics, Economic Buyer, Decision Criteria, Decision Process, Paper Process, Identify Pain, Champion):
- Evidence found (with specific quotes from sources)
- Confidence level (1-10)
- Risk flag (if confidence < 5)
- Suggested next action

Give me:
- Overall deal health rating (1-10)
- Top 3 risks
- Recommended immediate actions

Output as deal_scorecard.md.
```

## Customization Tips

- Adjust the criteria/structure to match your specific product and sales process
- Add or remove output fields based on what's useful for your workflow
- If the output is too long, add "Keep it under [N] words" to the prompt
- If you need a different output format, specify it (CSV, markdown, JSON)
