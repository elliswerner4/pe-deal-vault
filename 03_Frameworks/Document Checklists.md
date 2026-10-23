---
type: framework
up: "[[00_Home]]"
---
# Document Checklists (proactive upload prompts, by analytical phase)

Ask for documents proactively at each phase transition rather than working silently. The pattern is always: **"Here are documents that would materially sharpen [analysis X]. Want to upload any of them, or pass and I'll proceed with public sources / what's already uploaded?"**

Two principles:

1. **Always offer a "pass and continue" option.** The user is never blocked. If they pass, proceed with public sources and flags the analytical limitation as `[VERIFY]` / `[UNVERIFIED]` in the memo's open-question list.

2. **Batch upload requests at phase transitions, not piecemeal.** Don't interrupt every 30 seconds. Cluster all the documents that would sharpen the next analytical phase into one ask.

When asking, present the documents as a checklist the user can pick several from. Always include a "Pass — proceed with what I have" option.

---

## How to ask (canonical prompt template)

```
I'm about to {analysis_phase}. The following documents would materially sharpen
this work if you have them. Attach any you can share to the chat, or
pass and I'll proceed with public sources and flag the gaps.
☐ {doc 1} — would sharpen {what it sharpens}
☐ {doc 2} — would sharpen {what it sharpens}
☐ {doc 3} — would sharpen {what it sharpens}
☐ Pass — proceed with what I have
```

---

## Documents catalog by phase

The catalog below maps **each analytical phase** to the documents that would meaningfully sharpen it. Priority tags:

- **[ESSENTIAL]** — without this, the analysis is materially limited; flag the gap prominently
- **[STRONG]** — without this, analysis is qualitatively weaker but still useful
- **[NICE]** — marginal improvement; ask only if the user has volunteered

---

### Phase 1 — Intake / Orientation

Ask once at the very start, after the user has named the company:

| Document | Priority | What it sharpens |
|---|---|---|
| CIM (Confidential Information Memorandum) | **[ESSENTIAL]** for new deals; N/A for re-underwriting | Identity, financial highlights, growth thesis, asking valuation, named customers |
| Original IC memo from underwriting | **[ESSENTIAL]** for re-underwriting / portfolio monitoring | The thesis variance bridge anchor; entry valuation; original named risks |
| Banker teaser (if no CIM yet) | **[STRONG]** | Initial financial snapshot before the full CIM lands |
| Management presentation deck | **[STRONG]** | The narrative management uses with buyers; sales/growth claims |
| Prior screening memos for the same asset | **[NICE]** | Firm memory; what we thought last time we looked |

---

### Phase 2 — Financial Diligence (QofE-equivalent)

Before drafting the EBITDA bridge, returns analysis, or capital structure:

| Document | Priority | What it sharpens |
|---|---|---|
| Quality of Earnings (QofE) report | **[ESSENTIAL]** | Replaces public-data triangulation with audited adjustments; surfaces aggressive add-backs; sets the NWC peg basis |
| LBO / operating model (Excel) | **[ESSENTIAL]** | Gives driver-based revenue (volume × price × mix); explicit cost lines; sponsor's case |
| Audited financial statements (3-5 yrs) | **[ESSENTIAL]** | Anchors gross margin trajectory, EBITDA margin trend, working-capital pattern |
| Monthly P&L + BS + CF (trailing 24-36 months) | **[STRONG]** | Reveals seasonality, recurring vs. one-time, working-capital build/drain patterns |
| Customer cohort / NRR data tape | **[STRONG]** for SaaS / subscription businesses | Net retention, cohort retention curves, gross logo retention |
| Capital structure / debt agreement | **[STRONG]** | Existing debt to be refinanced; cov-lite vs. springing maintenance; LME blockers |
| Tax returns (3 years) | **[NICE]** | Cross-check on reported numbers; uncovers state-nexus exposure |

---

### Phase 3 — Commercial Diligence

Before market sizing, competitive analysis, customer-voice synthesis:

| Document | Priority | What it sharpens |
|---|---|---|
| Commercial Due Diligence (CDD) report | **[ESSENTIAL]** if available | Independent market sizing; customer interview synthesis; win/loss data |
| Customer list / contract roster | **[STRONG]** | Top-N concentration analysis (revenue AND gross profit); CoC consent triggers |
| Win/loss data tape | **[STRONG]** | Why customers buy vs. switch; primary purchase criteria |
| Sales pipeline (open opportunities + history) | **[STRONG]** | Pipeline coverage; rep ramp time; CAC payback |
| Reference call notes (from prior diligence) | **[NICE]** | Customer voice already captured by another party |
| Market research reports the firm has paid for | **[NICE]** | Sector context; competitive teardowns |

---

### Phase 4 — Legal / Regulatory Diligence

Before contract review, IP analysis, change-of-control mapping:

| Document | Priority | What it sharpens |
|---|---|---|
| Top 10 customer contracts | **[ESSENTIAL]** | CoC / anti-assignment risk; auto-renewal; MFN; LOL caps |
| Top 10 supplier contracts | **[STRONG]** | Sole-source risk; pricing volatility pass-through |
| Cap table (current) | **[ESSENTIAL]** | Options, warrants, pref stack, side letters |
| Litigation summary (pending + threatened) | **[STRONG]** | Reserve adequacy; material exposure |
| IP assignment agreements (employee + contractor) | **[STRONG]** for software | Chain-of-title; founders/contractors who own code |
| Disclosure schedule (if SPA-stage) | **[STRONG]** | Carve-outs already drafted; rep exceptions |
| Regulatory compliance docs (URAC, ACHC, DEA, FDA, etc.) | **[STRONG]** sector-dependent | Sector-specific risk |
| OFAC / sanctions screening | **[NICE]** | Customer / distributor sanctions exposure |

---

### Phase 5 — Management / Background Diligence

Before management assessment, MIP design:

| Document | Priority | What it sharpens |
|---|---|---|
| Org chart with named C-suite + comp | **[ESSENTIAL]** | Team depth; succession map; comp benchmarking baseline |
| Reference call notes (named + off-list refs for CEO/CFO) | **[STRONG]** | Backable-ness; conflict-handling; PE-experience signal |
| Background check results (if commissioned) | **[STRONG]** | Surprises (litigation, bankruptcy, regulatory ban) |
| Bios / resumes / LinkedIn URLs for top 5 execs | **[STRONG]** | Pattern-match against successful PE portcos |
| Comp benchmark study (Pearl Meyer / Radford / Mercer) | **[NICE]** | Gap analysis vs. market; retention package design |
| Equity rollover / MIP terms (from prior deals) | **[NICE]** | What the founder is willing to accept |

---

### Phase 6 — Tech / Cyber Diligence

Before architecture, security, OSS analysis (especially SaaS deals):

| Document | Priority | What it sharpens |
|---|---|---|
| SOC 2 Type II report (most recent) | **[ESSENTIAL]** for B2B SaaS | The baseline post-Change-Healthcare expectation |
| Penetration test results (recent ≤12mo) | **[STRONG]** | Critical-finding remediation status |
| Architecture documentation | **[STRONG]** | Scalability, multi-tenancy, tech-debt assessment |
| Vulnerability scan output (Black Duck, Snyk, Mend) | **[STRONG]** for software | OSS license risk; GPL contamination |
| Incident response playbook + prior incident logs | **[STRONG]** | Prior breach disclosure; IR maturity |
| Cyber insurance policy + limits | **[NICE]** | Coverage adequacy vs. exposure |
| Dev team headcount + tenure + attrition | **[NICE]** | Key-person engineering risk |

---

### Phase 7 — Portfolio Monitoring / Quarterly Variance

For existing portcos at quarterly cadence:

| Document | Priority | What it sharpens |
|---|---|---|
| Most recent monthly financials (3-12 mo trailing) | **[ESSENTIAL]** | Variance vs. plan, vs. IC underwrite case |
| Latest board materials | **[ESSENTIAL]** | Management commentary on variance drivers |
| KPI dashboard (current quarter) | **[ESSENTIAL]** | Cohort retention, customer count, NRR, headcount, etc. |
| Credit agreement covenant compliance certificate | **[STRONG]** | Headroom on each covenant; springing-test triggers |
| Add-on pipeline tracker (if applicable) | **[STRONG]** | Inorganic growth thesis status |
| Recent valuation mark draft (this quarter) | **[STRONG]** | Methodology continuity quarter-over-quarter |
| Customer renewal log (last 12 months) | **[STRONG]** | Top-N retention trajectory |

---

### Phase 8 — Re-Underwriting & Exit / CV Decision

In addition to portfolio monitoring docs above:

| Document | Priority | What it sharpens |
|---|---|---|
| Original IC memo (entry underwriting) | **[ESSENTIAL]** | Variance anchor; original entry valuation, growth assumptions, named risks |
| Original entry LBO / operating model | **[ESSENTIAL]** | Numerical thesis anchor; explicit projections to compare actuals against |
| All quarterly board materials over hold period | **[STRONG]** | Cumulative variance evidence; VCP progress tracking |
| Mark history (quarterly NAV each period) | **[STRONG]** | What the firm has been telling LPs vs. underwrite |
| For CV scenarios: proposed CV strike + sponsor analysis | **[ESSENTIAL]** | The CV valuation methodology to stress-test |
| For CV scenarios: fairness opinion draft (if available) | **[STRONG]** | Independent third-party benchmark |
| For CV scenarios: LPAC materials + ILPA governance docs | **[STRONG]** | Process + governance compliance |
| Buyer / strategic outreach history | **[NICE]** | Inbound interest signals; pricing data points |

---

## When NOT to ask

Don't prompt for uploads when:
- The user has explicitly said "just use public sources" or "do this from web only"
- The deal is at the screening / origination phase and the user just wants a quick triage
- The user has already volunteered the relevant document set up front
- The information has already been provided by an earlier upload in this session

In all four cases, proceed with what's available and note any analytical limitations in the memo's open-question list rather than re-asking.

## Recording the user's pass

Whenever the user passes on an upload, log the pass in the memo's **Open-Question / Diligence Gap List** with this format:

```
- [Limitation] {Phase X analysis} was conducted without {doc Y}. This means
  {specific limitation}. To upgrade this analysis, attach {doc Y} and re-run.
```

This preserves the audit trail: the user chose to proceed without the document; the memo shows what would have sharpened it.
