---
type: framework
up: "[[00_Home]]"
---
# House Style

The formatting, presentation and voice standard for every IC-grade output. It exists so every artifact reads, sources and reasons in one voice — and so an IC reader recognises the work in the first three seconds.

Replace `{{FIRM NAME}}` and `{{CITY}}` once, here, and every template inherits them.

**Order of precedence.** Where guidance conflicts: this file governs presentation and voice → the memo structure ([[_Memo Index]]) governs sections → [[Voice & Killer Slides]] governs exhibits → the mode file governs workflow. A memo structure may add sections; it may not override the rules below.

---

## 1. Document architecture

Every memo is built in five layers, in this order. Nothing is optional.

| Layer | Contents | Rule |
|---|---|---|
| 1 — Frontmatter | YAML block | Machine-readable; never rendered into the body |
| 2 — Header | The standard header block | §2 below, verbatim |
| 3 — Status panel | Draft status, readiness, key blockers | §3 below; **required on any memo not IC-ready** |
| 4 — Body | Numbered sections per the memo structure | §5–§8 below |
| 5 — Footer | Standard footer + blank sign-off lines | §2 below, verbatim; the memo **ends** here |

Anything after the footer is an **appendix** and must be labelled as such. Source registers, long schedules and raw exhibits go there.

### 1.1 Frontmatter

Every memo carries these keys. Use `[VERIFY]` for unknowns; never omit a key.

```yaml
---
type: memo
memo-type: screening | first-round-ic | final-ic | re-underwriting | variance
stage: <deal lifecycle stage>
status: draft | in-review | ic-ready | signed-off
deal: "[[<deal hub note>]]"
sector: "[[<sector playbook>]]"
date: YYYY-MM-DD
author: <name>
ic-ready: true | false
---
```

`status` and `ic-ready` are read together: a memo may be `status: draft` and `ic-ready: false` for weeks, but **no memo is circulated with `ic-ready: true` while any `{{TOKEN}}` remains unresolved** (§9).

---

## 2. Header and footer

Open every memo with this block, verbatim. Field names, order and column alignment do not vary.

```
══════════════════════════════════════════════════════════════
{{FIRM NAME}}
{{MEMO TYPE}}
──────────────────────────────────────────────────────────────
CONFIDENTIAL & PRIVILEGED | FOR INTERNAL IC USE ONLY
──────────────────────────────────────────────────────────────
Deal:               {{deal name}}
Mode:               {{mode}}
Lead Partner:       {{lead partner}}
Fund:               {{fund}}
Prepared by:        {{author}} (AI-assisted where applicable)
Date:               {{date}}
══════════════════════════════════════════════════════════════
```

Close every memo with this block, verbatim.

```
──────────────────────────────────────────────────────────────
{{FIRM NAME}} | {{CITY}}
Confidential — Not for External Distribution

Every numeric output carries a shown derivation or a registered
source; qualitative claims are cited inline. Final valuation
conclusions and investment recommendations require human IC sign-off.

Sign-off — Lead Partner:    _________________________   Date: __________
Sign-off — IC Member 1:     _________________________   Date: __________
Sign-off — IC Member 2:     _________________________   Date: __________
══════════════════════════════════════════════════════════════
```

**Permitted footer addition.** Re-underwriting memos covering a continuation vehicle or other fund-to-fund transaction insert one paragraph above the sign-off lines stating that the valuation conclusion is conflicted by construction and requires human IC sign-off. This is the only sanctioned deviation from the block.

**Unknown header fields** are written `[VERIFY]`, never fabricated and never left blank.

---

## 3. Status panel

Any memo that is not IC-ready opens — immediately after the header, before section 1 — with a blockquote status panel. It answers three questions in under 150 words: what was this built from, what is missing, and what must happen before it circulates.

```markdown
> **Draft status.** <one sentence on what the memo was built from.>
>
> **Readiness:** <n> of <n> required exhibits complete · **Not IC-ready.**
>
> **Blocking:** <the two or three documents that unblock the most.>
>
> `[Limitation]` <the consolidated limitation line, per §7.>
```

A memo that *is* IC-ready omits the panel and sets `ic-ready: true` in frontmatter.

---

## 4. Navigation

- **Contents block required** on any memo over five sections. Place it directly after the status panel; link every top-level section; one line per section, no descriptions.
- **Cross-references use section numbers**, not page numbers or titles: "see §11.4", not "see the conflicts map above."
- **Sections are numbered in the body** as `## 1. Executive Summary & Recommendation`. Subsections carry the parent number: `### 11.4 Conflicts map`.

---

## 5. Headings, emphasis and rules

| Element | Rule |
|---|---|
| H1 | Once per note, immediately after the header block. The deal and memo type. |
| H2 | Numbered top-level sections only |
| H3 | Numbered subsections only |
| H4 | Avoid. If a subsection needs subdivision, it is a table or a list. |
| Horizontal rule | Between top-level sections only. Never inside a section. |
| **Bold** | The load-bearing clause of a paragraph, and grades. Not for emphasis-by-volume — if three things in a paragraph are bold, none of them are. |
| *Italic* | Defined terms on first use, and scenario labels (*we are wrong if…*). Not for emphasis. |
| `Code ticks` | Confidence tags, `[Limitation]` markers, tokens, field names, file paths. Nothing else. |
| Blockquote | Callouts only, per §6 |

---

## 6. Callouts

Four callout types. Each opens with a bolded label so it reads correctly in Obsidian, in Word, and in plain text. No other blockquote use.

```markdown
> **Finding.** <the conclusion, then the evidence.>

> **Caution.** <a number or claim that will mislead if read at face value.>

> **Blocked.** <what cannot be concluded, and the document that unblocks it.>

> **Decision required.** <what the IC must decide, and by when.>
```

Use them sparingly — at most one per section. A callout on every page is a document with no hierarchy.

---

## 7. Claims, numbers and citations

These are the rules that make the work checkable. They are not stylistic.

### 7.1 Confidence tags

Every non-trivial claim carries exactly one:

| Tag | Means | Test |
|---|---|---|
| `[FACT]` | Verifiable from a named source or shown arithmetic | Could a reader confirm it from the citation alone? |
| `[REPORTED]` | Asserted by a party with an interest — company, sponsor, management | Who benefits if this is believed? |
| `[ESTIMATE]` | Our number, from stated inputs and a stated method | Is the method shown? |
| `[INFERENCE]` | Our reasoning from facts stated elsewhere in the memo | Are the premises in the document? |
| `[VERIFY]` | Not established; a named open item | Is it in the open-question list? |

A `[FACT]` with no citation is a defect. A number that a source does not actually support is a defect, even where a source is cited.

### 7.2 Numbers

- **Units always.** `$M`, `$B`, `×`, `%`, `bps`, `days`. Never a bare figure.
- **Source or derivation always.** Cite it, or show it: `6.45 years — derived: 2,355 days ÷ 365.25`.
- **Derived figures show their inputs.** A number that cannot be recomputed from what is on the page is not derived, it is asserted.
- **Ranges beat false precision.** Where only a year is sourced, give the range the year permits and tag `[ESTIMATE]`.
- **Consistency across sections.** A figure stated twice is stated identically. Rounding is fixed on first use.
- **Thresholds are cited too.** "Above 95% retention" carries the source of the 95%.

### 7.3 Citations

Inline, in ticks, at the end of the sentence or table cell:

`[Source: filename or URL, section or date]`

Repeat citations within a table rather than writing "ibid." or "same as above" — except in a source column, where `same` is permitted for an immediately preceding identical source.

Every external source appears once in the **Appendix — Source register**, numbered, grouped by category, with full URL.

### 7.4 Limitations

Every skipped or unavailable document is logged, in this exact sentence shape:

> `[Limitation]` {phase} was conducted without {documents}. This means {the specific analytical consequence}.

Three rules: the consequence is specific ("the thesis-vs-actuals bridge was not built"), never generic ("analysis may be incomplete"); the limitation sits at the foot of the section it constrains; and all limitations are consolidated again in the open-question section.

---

## 8. Tables and exhibits

### 8.1 Tables

- Use a table only where it communicates better than a sentence. Two rows is a sentence.
- **Every table has a header row**; every column has a unit in the header where a unit applies (`Revenue ($M)`, not `Revenue`).
- **Every table has a source or confidence column**, or per-cell tags. A table of untagged numbers is not IC-grade.
- Empty cells are `—`, never blank. Unknown cells are `[VERIFY]`, never `—`.
- Keep tables under eight columns. Wider than that, split them or move to an appendix.
- Order rows by the reader's question, not by the order the data arrived: most material first.

### 8.2 Exhibits

Exhibits are the numbered artefacts of [[Voice & Killer Slides]]. Label them in the body as **Exhibit N — Title**, keep the numbering identical to the killer-slide list, and carry a status table in the recommendation section:

| Status | Means |
|---|---|
| **Complete** | Built, populated, sourced |
| **Partial** | Built, partly populated; the gap is named |
| **Blocked** | Structure built, no inputs; the unblocking document is named |

The status table's counts must reconcile with the rows above it. A stated count that contradicts its own table is a defect.

### 8.3 Grade and status vocabulary

Fixed vocabulary; no synonyms.

| Context | Permitted values |
|---|---|
| Eight-question grades | **strengthened / held / weakened / broken / withheld** |
| Initiative progress | **delivered / partial / missed / not yet pursued** |
| Risk movement | **improved / unchanged / worsened / new** |
| Exhibit status | **complete / partial / blocked** |
| Confidence | **high / medium-high / medium / low** |

"Withheld" is used where the original claim is unavailable — it is an honest non-answer, not a failure, and it must name what would allow the grade.

---

## 9. Placeholders and tokens

- `{{TOKEN}}` marks a firm-level value set once in this file (`{{FIRM NAME}}`, `{{CITY}}`, the mandate block).
- `[VERIFY]` marks a deal-level unknown. These are different things and are never interchanged.
- **A memo may be drafted with unresolved tokens. It may not be circulated with them.** Resolving every `{{TOKEN}}` is a precondition of `ic-ready: true`.
- Unresolved `[VERIFY]` items are permitted at IC — that is what the open-question list is for — provided each appears there with an owner and a deadline.

---

## 10. Voice

1. **Rigorous and calibrated.** Confidence-tag every non-trivial claim. Never overstate.
2. **Candid, not promotional.** No "obviously," "clearly," "robust," "comprehensive," "world-class." If something is good, the evidence makes it good; the words do not.
3. **No hype.** No emojis, no exclamation marks.
4. **Bury nothing.** Executive summary in the first 200 words. Recommendation at the top, not the bottom.
5. **Honest pre-mortem.** Every memo includes a "What would make us wrong" section, and every bullet in it carries a confidence tag.
6. **Every number has units and a source.** Cited or derived, never bare.
7. **Variance, not re-narration.** Say what changed against what was claimed, and by how much. A paragraph that restates the business is not analysis.
8. **Name the decision.** Every memo ends on a recommendation with the conditions that would change it.

Writing posture: a senior associate writing for an IC of partners who have read a thousand of these. Assume they will check the arithmetic.

---

## 11. Mandate framing (fill in for your firm)

Every screening memo grades the target against the firm's mandate. Define it once here:

- **Sectors in mandate:** {{e.g., healthcare services, business services, industrial growth}}
- **Size band:** {{e.g., $3M-$25M EBITDA platforms}}
- **Geography:** {{e.g., US + selective Canada}}
- **Deal type:** {{e.g., founder recaps / MBOs; no carve-outs}}
- **Structure posture:** {{e.g., conservative leverage <3.5×; 20-40% management rollover}}
- **Hold period:** {{e.g., 5-7 years}}
- **Exit channels:** {{e.g., strategic primary; sponsor-to-sponsor; CV for long-hold assets}}

---

## 12. File naming and location

- **Memos:** `{{Deal}} — {{Memo type}} ({{YYYY-MM-DD}}).md`, stored in the deal folder beside the hub note.
- **Hub notes:** the deal name exactly, so `[[wikilinks]]` resolve without aliases.
- **Exports:** same basename, different extension. A `.docx` or `.pdf` export never diverges from its markdown source — regenerate, do not hand-edit.
- Dates are ISO (`YYYY-MM-DD`) everywhere: filenames, frontmatter, tables, body text.

---

## 13. Pre-delivery checklist

Run before any memo leaves the drafter. Each line is a defect class seen in practice.

**Structure**

- [ ] Header block verbatim; every field filled or `[VERIFY]`
- [ ] Status panel present, or `ic-ready: true`
- [ ] Contents block present (memos over five sections)
- [ ] Every section of the memo structure present, numbered, in order
- [ ] Footer verbatim, with blank sign-off lines; memo ends there
- [ ] Appendices labelled as appendices

**Claims and numbers**

- [ ] Every non-trivial claim carries exactly one confidence tag
- [ ] No `[FACT]` without a citation or shown arithmetic
- [ ] No bare numbers — units, plus source or derivation
- [ ] Every derived figure recomputable from inputs shown on the page
- [ ] Figures stated in more than one section agree
- [ ] Every threshold cited
- [ ] Every `[Limitation]` in the mandated sentence shape, with a specific consequence

**Analysis**

- [ ] Recommendation in the first 200 words
- [ ] "What would make us wrong" present, every bullet tagged
- [ ] Grades drawn from the §8.3 vocabulary
- [ ] Exhibit status table reconciles with its own rows
- [ ] Open-question list carries question, why it matters, owner, deadline
- [ ] All red-flag triggers dispositioned — applied, or explicitly marked not applicable

**Voice and presentation**

- [ ] No banned words, emojis or exclamation marks
- [ ] One H1; no H4
- [ ] Tables carry units and sources; no blank cells
- [ ] At most one callout per section
- [ ] All `{{TOKEN}}` resolved if `ic-ready: true`
- [ ] Source register complete, numbered, with full URLs

---
Related: [[_Memo Index]] · [[Voice & Killer Slides]] · [[The 8-Question Framework]] · [[Red-Flag Triggers]] · [[Document Checklists]]
