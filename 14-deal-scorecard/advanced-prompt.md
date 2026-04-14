# MEDDPICC Deal Risk Scorecard — Advanced Prompt

For GTM engineers and operators who want configurable scoring, batch analysis, and structured output.

## Prerequisites

- Claude Code installed
- Deal artifacts (transcripts, CRM notes, emails) dumped into a single folder
- No folder structure needed — just dump everything in one place, Claude Code figures out which files belong to which deal

---

## 1. Configurable Single-Deal Scorecard

Customize the criteria definitions and weights for your org MEDDPICC framework.

```
Read all files in /deals/.

Score this deal against MEDDPICC using these definitions:

M - Metrics: Has the prospect quantified the business impact?
  10 = specific dollar or percent impact stated by prospect
  5 = vague we need to improve
  1 = no metrics discussed

E - Economic Buyer: Is the EB identified and engaged?
  10 = EB on a call, expressed support
  5 = EB identified but not engaged
  1 = unknown who the EB is

D - Decision Criteria: Do we know how they will evaluate?
  10 = written evaluation criteria shared
  5 = verbally discussed preferences
  1 = no criteria discussed

D - Decision Process: Do we know the steps to close?
  10 = documented process with timeline
  5 = general sense of steps
  1 = we will figure it out

P - Paper Process: Do we know procurement/legal steps?
  10 = legal involved, timeline known
  5 = aware of procurement but no timeline
  1 = not discussed

I - Identify Pain: Is the pain clearly articulated?
  10 = prospect described pain with specifics
  5 = acknowledged a general problem
  1 = we are pushing a solution they did not ask for

C - Champion: Do we have an internal advocate?
  10 = actively selling internally, giving us intel
  5 = supportive but passive
  1 = no champion identified

Weights (adjust for your org):
  M: 10%, E: 20%, D: 10%, D: 10%, P: 10%, I: 15%, C: 25%

For each criterion:
- Score (1-10)
- Evidence (exact quote or reference from the files)
- Confidence in the score (HIGH / MED / LOW)
- Risk flag if score < 5
- Specific next action to improve this score

Output:
- Weighted overall score
- Top 3 risks ranked by (weight x gap)
- Recommended actions prioritized by impact
- Deal verdict: STRONG / ON TRACK / AT RISK / DEAD

Output as deal_scorecard.md
```

---

## 2. Batch Mode — Score Multiple Deals at Once

Dump all your deal files into one folder. Do not organize them. Claude Code sorts it out.

```
Read all files in /pipeline-review/.

These files are from multiple deals — transcripts, CRM notes,
emails, mixed together. Figure out which deal each file belongs
to based on company names, participants, and context. Group
them by deal.

Score each deal against MEDDPICC using these weights:
  M: 10%, E: 20%, D: 10%, D: 10%, P: 10%, I: 15%, C: 25%

Output a comparison matrix as pipeline_scorecard.csv:
- Columns: Deal, M, E, D, D, P, I, C, Weighted Score, Verdict, Top Risk, Next Action
- Sort by weighted score ascending (worst deals first)

Also output pipeline_summary.md with:
- How many deals at each verdict level
- The 3 deals that need immediate attention and why
- Common gaps across the pipeline (e.g., 5 of 8 deals have no EB engagement)
```

---

## 3. Structured Output Options

### JSON (for dashboards, Notion, or downstream tools)

Add this to any prompt above:
```
Output as JSON with this schema:
{
  deal: string,
  scores: {
    metrics: {score: int, evidence: string, confidence: string},
    economic_buyer: {score: int, evidence: string, confidence: string},
    decision_criteria: {score: int, evidence: string, confidence: string},
    decision_process: {score: int, evidence: string, confidence: string},
    paper_process: {score: int, evidence: string, confidence: string},
    identify_pain: {score: int, evidence: string, confidence: string},
    champion: {score: int, evidence: string, confidence: string}
  },
  weighted_score: float,
  verdict: string,
  top_risks: [string],
  next_actions: [string]
}
```

### CSV (for spreadsheet analysis)

Add this to any prompt above:
```
Output as CSV with columns:
Deal, Metrics, Economic_Buyer, Decision_Criteria, Decision_Process,
Paper_Process, Identify_Pain, Champion, Weighted_Score, Verdict,
Top_Risk, Next_Action
```

---

## 4. Delta Scoring — Track Changes Over Time

After running a scorecard once, save the output. Next review cycle:

```
Read all files in /deals/.

Here is last month scorecard for this deal:
[paste previous scorecard output here]

Now read any new files added since last review.

Show me:
- What changed (criterion by criterion)
- What improved (with evidence)
- What regressed (with evidence)
- Updated weighted score
- Whether the verdict changed

Output as deal_scorecard_delta.md
```

---

## Customization

- Change the weights to match what matters in your sales motion. High-ACV enterprise? Weight EB and Paper Process higher. PLG-to-sales? Weight Champion and Pain higher.
- Add custom criteria — some orgs add Competition or Timeline as explicit criteria. Just add them to the prompt with the same format.
- Change the verdict thresholds — default: STRONG (8+), ON TRACK (6-8), AT RISK (4-6), DEAD (below 4). Adjust for your close rates.
- Pipe the CSV output into your forecasting tool or Notion database for a live pipeline health dashboard.
