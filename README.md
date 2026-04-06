# Claude Code for Sales — 31 Use Cases

**One prompt. One input. One output. Every use case reviewed by a human before it goes anywhere.**

I work with the GTM teams of some of the fastest-growing dev tools in the world. This repo is a collection of Claude Code workflows I've built for sales teams — tested against real scenarios, documented with exact prompts.

## The Philosophy

- **Input is a file.** A CSV, a transcript, a PDF, a URL.
- **Output is a file.** A scored list, a deal brief, a battlecard, an email draft.
- **Human reviews before acting.** Every output gets checked before it reaches a buyer.

Low risk. High leverage. The boring 80% of sales — done in minutes.

## Prerequisites

1. [Install Claude Code](https://docs.anthropic.com/en/docs/claude-code) (5 minutes)
2. Have access to the sales tools you already use (Salesforce, Gong, etc.)
3. That's it. No APIs. No integrations. No IT tickets.

## Use Cases

| # | Use Case | Sales Stage | Input | Time Saved |
|---|----------|-------------|-------|------------|| 1 | [ICP Lead Scoring](./01-icp-scoring/) | Prospecting | CSV of leads | 4 hrs → 60 sec |
| 2 | [Account Research One-Pager](./02-account-research/) | Pre-call Research | Company URL | 25 min → 90 sec |
| 3 | [Deal Status Extraction](./03-deal-status/) | Deal Intelligence | Gong transcripts | 3 hrs → 2 min |
| 4 | [Follow-Up Email from Notes](./04-followup-email/) | Outreach | Call notes | 15 min → 30 sec |
| 5 | [Stale Deal Detector](./05-stale-deals/) | Pipeline Hygiene | Salesforce CSV | 45 min → 30 sec |
| 6 | [Competitive Battlecard](./06-battlecard/) | Competitive Intel | Competitor URLs | 1 hr → 3 min |
| 7 | [Job Posting Intent Mining](./07-intent-signals/) | Prospecting | Job descriptions | ongoing → 2 min |
| 8 | [Champion vs EB Alignment](./08-alignment-check/) | Deal Intelligence | 2 transcripts | manual → 90 sec |
| 9 | [CRM Name Cleanup](./09-crm-cleanup/) | Pipeline Hygiene | CRM column CSV | never done → 20 sec |
| 10 | [10-K Executive Brief](./10-10k-analyzer/) | Pre-call Research | 10-K PDF | 200 pages → 90 sec |
| 11 | [Personalized First Lines](./11-first-lines/) | Outreach | Prospect CSV | 3-5 hrs → 5 min |
| 12 | [Lost Deal Reason Analyzer](./12-lost-deals/) | Reporting | Closed-lost CSV | hours → 2 min |
| 13 | [G2 Review Sentiment](./13-g2-sentiment/) | Competitive Intel | Copy-pasted reviews | hours → 90 sec |
| 14 | [MEDDPICC Deal Scorecard](./14-deal-scorecard/) | Deal Intelligence | Transcripts + CRM | 45 min → 2 min |
| 15 | [LinkedIn Prospect Deep Dive](./15-linkedin-deepdive/) | Pre-call Research | Profile text | 20 min → 60 sec |
| 16 | [Win/Loss Analysis](./16-win-loss/) | Reporting | Quarterly CSV | full day → 3 min |
| 17 | [Analyst Report → Accounts](./17-report-accounts/) | Prospecting | Analyst PDF | 2 hrs → 2 min |

*More use cases being added daily. Star ⭐ to follow along.*

## How Each Use Case Works

Every folder contains:
- **README.md** — What it does, what you need, step-by-step walkthrough
- **prompt.md** — The exact prompt to copy-paste into Claude Code
- **template or sample files** — Output templates or sample input structure (where applicable)

## Author

**Pratyush Kukreja** — GTM operator, 3x founder ($0→$15M+ ARR), author of *Uplift* (B2B SaaS sales).

Currently working with sales teams at some of the fastest-growing dev tools in the world.

[LinkedIn](https://linkedin.com/in/pratyushkukreja) · [Twitter/X](https://x.com/pratyushkukreja)
