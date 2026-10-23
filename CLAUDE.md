# PE Deal Vault — standing instructions

This folder is a private-equity deal knowledge system. It holds the firm's house style, memo structures, sector playbooks, red-flag triggers and analysis templates as plain markdown. Read them before you produce anything. Write your output back into this vault as properly-linked markdown.

## Read first — every session, before drafting

Before drafting any deal artifact, read:

1. `03_Frameworks/House Style.md` — voice, header, footer, mandate, citation rules
2. `03_Frameworks/Deal Lifecycle.md` — which stage produces which artifact
3. The relevant `03_Frameworks/Mode — *.md` — the workflow for this stage
4. The matching structure in `03_Frameworks/Memos/` — the section list
5. The relevant playbook in `04_Sectors/` — KPIs, red flags, regulatory lenses, comp sources

Do not ask me to explain the house style, the memo structure, or the sector KPIs. They are in this folder. If something genuinely isn't here, say so and proceed with a flagged assumption.

## Pick a mode from what I give you

| What I give you | Mode to run | Output |
|---|---|---|
| A bare company name | Screening | 1-2 page screening memo |
| A CIM or teaser | Screening (upgrade to First-Round IC on request) | 1-2 pages, then ~15 |
| CIM + "we're bidding" | First-Round IC | ~15 page memo + LBO sketch |
| LOI signed / diligence materials | Diligence & Exclusivity | Final IC memo, 30-35 pages |
| Original IC memo + current financials | Re-Underwriting | 15-25 page memo |
| A quarter's board pack | Quarterly Monitoring | 3-5 page variance report |

State which mode you picked in one line before you start. If it's ambiguous, pick the lighter one and say why.

## Non-negotiables

- **Confidence-tag** every non-trivial claim: `[FACT]` / `[REPORTED]` / `[ESTIMATE]` / `[INFERENCE]` / `[VERIFY]`
- **Never a bare number.** Units plus a citation or a shown derivation. Every time.
- **Recommendation first.** Executive summary in the first 200 words. Bury nothing.
- **"What would make us wrong"** section in every memo. Write the real bear case, not a token one.
- **Open-question list** at the end: question, why it matters, who to ask, deadline.
- **Sign-off lines stay blank.** Never sign for a human. For continuation-vehicle or fund-to-fund transactions, never conclude valuation autonomously — the transaction is conflicted by construction.
- **Check the 10 red-flag triggers** in `03_Frameworks/Red-Flag Triggers.md` against every draft. Depth matters here: **at screening, log what fires in the memo's red-flag section, state the question it raises, and keep going** — a screen that halts to ask five questions has failed at its one job. **From first-round IC onward, stop and surface everything that fired in a single prompt** before continuing. Never piecemeal.
- **Log every skipped document** as `[Limitation] {phase} was conducted without {doc}. This means {specific limitation}.` Never a silent gap.

## Where output goes

- Deal artifacts → `01_Deals/<Deal Name>/`, alongside the deal hub note
- Portfolio artifacts → `02_Portfolio/<Company>/`
- Any new multiple you encounter → append a dated, cited row to `07_Market Intel/Comps Log.md`
- Any named person or firm → a note in `06_People & Firms/` from the matching template
- Filenames follow House Style: `{{Firm}}_{{Deal}}_{{mode}}_{{YYYY-MM-DD}}`

Update the relevant index note (`_Deal Index`, `_Portfolio Index`) whenever you add something. Update `00_Home.md`'s active-work table when a deal's stage changes.

## Linking discipline

Every company, person, firm, sector and framework you mention in a new note gets an Obsidian `[[wikilink]]` — **even if the target note does not exist yet.** An unresolved link is a to-do, and the accumulating link graph is the entire point of the system. Two years in, opening a sector note should show every deal seen in that space; opening a banker's note should show every process they've run.

## Ask before you guess

Ask me for documents at phase transitions, batched into one request, per `03_Frameworks/Document Checklists.md`. Always offer a "pass and proceed with public sources" option — I should never be blocked. If I pass, proceed and log the `[Limitation]`.

## What not to do

- Don't soften a red flag to be agreeable. The value of this system is that it says the uncomfortable thing early.
- Don't fabricate a source, a figure, or a comp. Write `[VERIFY]` and tell me what would resolve it.
- Don't produce screening depth on a final-bid deal, or final-bid depth on a screen. Match the artifact to the stage.
- Don't use marketing language. No "obviously," "clearly," "robust," "comprehensive," "world-class." No emojis, no exclamation marks.
