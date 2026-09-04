# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this repository is

A structured technology watch (*veille technologique*) program for a development team. All content is in **French**. There is no code, no build system, and no tests — the entire repo is Markdown documentation.

## File structure and purpose

| File / Directory | Purpose |
|---|---|
| `01-domaines-sources.md` | 9 priority domains, each with curated sources (max 5/developer) — domain 9 (personal finance/investing) is informational only and does not feed the tech radar |
| `02-fiche-evaluation.md` | Canonical template for technology evaluation sheets + filled example |
| `03-rituels.md` | Meeting calendar: bi-weekly Tech Talk, monthly Brown Bag, quarterly Hack Day + Radar update |
| `04-tech-radar.md` | The live team radar (4 rings: Adopt / Trial / Assess / Hold), updated each quarter |
| `fiches/` | Filled evaluation sheets, one file per technology |
| `archives/` | Previous radar snapshots, named `radar-YYYY-QX.md` |

## Naming conventions

- Evaluation sheets in `fiches/`: use kebab-case matching the technology name, e.g. `fiches/bun-1x.md` or `fiches/api-platform-3.md`
- Radar archives: `archives/radar-YYYY-QX.md` (e.g. `archives/radar-2026-Q3.md`)

## Radar quadrants and rings

**Quadrants:** Langages & Frameworks · Infrastructure & Cloud · Intelligence Artificielle & ML · DevOps & Observabilité

**Rings:**
- **ADOPT** — production-ready, use by default on new projects
- **TRIAL** — promising with positive POC(s), use on non-critical projects
- **ASSESS** — worth watching, invite exploration and personal POCs
- **HOLD** — do not start new projects; existing projects may stay

## Workflow for adding a new technology

1. Post in `#veille-tech` Slack with tag `[RADAR-PROPOSE]`
2. Create a filled fiche in `fiches/` using the template from `02-fiche-evaluation.md` (required: sections 1, 3, 8; section 7 if a POC was done)
3. Present at the next Tech Talk or Brown Bag
4. Vote at the quarterly radar review → update `04-tech-radar.md` + archive the previous version

**Governance thresholds:** Adopt requires 80% agreement; Trial/Assess/Hold require 60%; quorum is 50% of the team present.

## Quarterly schedule

Radar reviews: **first week of March, June, September, December**. The Hack Day precedes it by one week (last Friday of month 3 in the quarter).

## Current tech radar snapshot (Q2 2026)

The radar was last updated **2026-06-08**. Next review: **2026-09-07**. Notable recent moves: LangChain (Trial → Adopt), Bun (Assess → Trial), OpenTofu (Hold → Trial), Jenkins (Adopt → Hold).

Primary stack on radar: PHP 8.3+ / Symfony 7.x / TypeScript / React 19 / Python 3.12+ / Go 1.22+ on AWS EKS with GitHub Actions CI/CD.
