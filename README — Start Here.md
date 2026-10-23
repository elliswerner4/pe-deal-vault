---
type: readme
---
# PE Deal Vault — Start Here

A working knowledge system for private equity / investment banking deal work, built for [Obsidian](https://obsidian.md) (free, local, offline). Everything is plain markdown on your own disk — nothing leaves your machine, no plugins required, no cloud dependency. That also makes it firm-firewall-friendly by construction.

## Setup (2 minutes)

1. Download Obsidian, then **Open folder as vault** → select this `PE Deal Vault` folder.
2. Settings → Core plugins → make sure **Templates** is on. Settings → Templates → set folder to `99_Templates`.
3. Open [[00_Home]] and pin it. Done.

## How it's organized

| Folder                | What lives there                                                                                                                                                                |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| `00_Home`             | The dashboard — start every session here                                                                                                                                        |
| `01_Deals`            | One folder per deal: hub note + memos + meeting notes                                                                                                                           |
| `02_Portfolio`        | Companies under recurring monitoring: dossiers + dated briefings                                                                                                                |
| `03_Frameworks`       | The thinking system: [[Deal Lifecycle]], [[The 8-Question Framework]], [[Red-Flag Triggers]], [[Document Checklists]], [[Monitoring Cadence]], [[House Style]], memo structures |
| `04_Sectors`          | Six sector playbooks — KPIs, red flags, regulatory lenses, comp sources                                                                                                         |
| `05_Analysis Library` | Fill-in analytical tables: EBITDA bridge, NWC peg, net debt, LBO, sensitivities, risk matrix                                                                                    |
| `06_People & Firms`   | One note per person and firm — backlinks build your relationship map automatically                                                                                              |
| `07_Market Intel`     | Comps log, precedent transactions, banker coverage — your accumulating market memory                                                                                            |
| `99_Templates`        | Insert with the Templates command when creating new notes                                                                                                                       |

## The core idea

Deals are temporary; **pattern recognition compounds**. Every deal note links to the sector playbook it stressed, the people it involved, the comps it produced, and the red flags it fired. Two years in, opening a sector note shows every deal you've seen in that space; opening a banker's note shows every process they've run at you. Dead deals stay in the vault as firm memory — the next time the asset trades, you already have a view.

## Conventions (the whole system in five rules)

1. **Everything that has a name gets a `[[wikilink]]`** — companies, people, firms, sectors. Links are free; backlinks are the payoff.
2. **Frontmatter on every note** (`type`, `stage`, `status`...) so search and future plugins can slice the vault.
3. **Claims carry tags** — `[FACT]` / `[REPORTED]` / `[ESTIMATE]` / `[INFERENCE]` / `[VERIFY]` — per [[House Style]].
4. **Numbers are never bare** — units + source or shown derivation.
5. **Passes are logged** — skipped diligence documents become explicit `[Limitation]` lines, not silent gaps.

## Make it yours

- Fill in `{{FIRM NAME}}`, `{{CITY}}`, and the mandate block in [[House Style]] — every template inherits it.
- Delete the example deal (`01_Deals/Ridgeline Infusion Partners (Example)/`) once you've created your first real one.
- Optional power-ups, in order of value: **Dataview** community plugin (auto-generating deal/portfolio tables from frontmatter), **Templater** (smarter templates), **Kanban** (pipeline board). The vault works fully without them.
- Works well with an AI assistant: the frameworks in `03_Frameworks` are written so they can be pasted into an AI chat as instructions, and AI-drafted memos can be saved straight into deal folders — every claim tagged and cited per [[House Style]].
