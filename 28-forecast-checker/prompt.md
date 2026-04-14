# Forecast Sanity Checker — Prompt

Copy-paste this into Claude Code.

```
Read forecast.csv.

For each commit deal, cross-reference with activity logs and transcripts.
Score deal signals:
- Recent activity (last 7/14/30 days)
- Stakeholder engagement
- Next steps quality
- Timeline alignment

Flag deals where forecast category does not match signals.
For each flag: explain why, recommend upgrade/downgrade/validate.

Output as forecast_audit.md.
```

## Customization

- Adjust criteria to match your sales process
- Change output format if needed (CSV, JSON, markdown)
- Add or remove fields based on what is useful for your workflow
