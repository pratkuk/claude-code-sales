# ICP Scoring Prompt

Copy-paste this into Claude Code. Edit the ICP definition for your product.

```
Read leads.csv.

Score each lead against this ICP:
- B2B SaaS company
- 50-500 employees
- Series A through Series C funding
- Selling to NA or EU markets

Add columns:
- ICP_Score (1-10)
- Reasoning (one sentence explaining the score)
- Priority_Tier (Tier 1 = 8-10, Tier 2 = 5-7, Tier 3 = 1-4)

Sort by ICP_Score descending.
Output as scored_leads.csv.
```

## Customization Tips

- Change the ICP criteria to match your actual product
- Add more criteria: tech stack, revenue range, specific industries
- Adjust tier thresholds based on your team's capacity
- Add a "Disqualified" tier for leads that are clearly outside ICP
