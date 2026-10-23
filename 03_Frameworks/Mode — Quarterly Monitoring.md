---
type: framework
tags:
  - mode
up: "[[Deal Lifecycle]]"
---
# Mode: Quarterly Monitoring

**Trigger.** Quarterly cadence; portco financials posted. Run on demand when the user attaches the quarter's materials.

**Deliverable.** Variance-vs-Thesis Report (3-5 pages, structure: [[Memo — Variance Report]]).

**Workflow.**
1. Ingest whatever the user attaches: financials, KPI dashboard, board materials.
2. Compute variance vs. the IC base case for the 7-10 KPIs that matter for this portco's thesis.
3. Identify the top 3 variances and hypothesize drivers from board commentary.
4. Covenant ratio computation + threshold check (headroom <20% is a watch-list flag).
5. Roll the valuation mark forward using the prior-quarter methodology.
6. Compose the report; always include 2-3 specific decisions the partner needs to make this quarter.

**Recurring monitoring (optional).** Where the user's Claude workspace supports scheduled/recurring tasks, the same scan can run on a cadence: daily material-news alerts (alert-only — skip PR puffery), weekly company intel, monthly regulatory/sector scan, quarterly variance, semi-annual leadership scan, annual exit-readiness. Cadence matches how fast each variable moves; materiality determines what gets surfaced vs. silently logged. Watch-list companies (covenant stress, post-close first year, exit window year 4+) get tightened cadence.
