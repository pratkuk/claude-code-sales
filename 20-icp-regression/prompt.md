# ICP Scorecard via Regression — Prompt

Copy-paste this into Claude Code.

```
Read deals_history.csv.

Run logistic regression on win/loss outcome against all attributes.
Tell me which attributes are statistically significant predictors.
Build a weighted scorecard from the coefficients.
Test against a 20% holdout set.
Score my current pipeline with the model.

Output three files:
1. icp_scorecard.md — the weighted model explained in plain English
2. scored_deals.csv — every deal re-scored with predicted vs actual
3. model_summary.md — accuracy %, top 5 predictors, surprises
```

## Customization

- Adjust criteria to match your sales process
- Change output format if needed (CSV, JSON, markdown)
- Add or remove fields based on what is useful for your workflow
