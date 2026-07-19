# Business Finance Pro — Release Notes
## Version 1.0.0 (Macro-Free Edition)

---

## Overview

This is the first production release of Business Finance Pro: a complete, self-contained financial operating system for small business owners, built entirely inside a single Excel workbook with no macros, no VBA, and no external dependencies.

## What's Included

**Six visible screens:** Home Dashboard, Settings, Quick Add, Bills, Clients, Goals

**Four calculation engines**, all formula-only, rule-based, zero AI:
- `_calc_Core` — shared financial metrics (Money In/Out, Net Cash Flow, Transaction Count, Average Transaction)
- `_calc_Health` — a weighted-component Business Health scoring engine
- `_calc_Attention` — a prioritized, ranked action-item engine (up to 5 items)
- `_calc_Insights` — a Top-3 narrative insight engine powering the Home dashboard's "This Week" briefing

**A complete, protected data layer:** nine Excel Tables covering Transactions, Categories, Vendors, Bills, Customers, Invoices, Goals, Business Profile, and Settings — every hidden sheet fully locked, every dropdown backed by a reusable named validation list.

**106 named ranges** forming the sole interface between the data layer, calculation engines, and presentation layer — no visible screen references a hidden table directly, with one documented exception (see Known Limitations).

## Verified Quality

This release passed two full audit cycles before shipping:

1. **RC1 Audit** — a structural and functional review against the original product requirements, data model, and every development sprint's stated scope. Found and fixed two bugs: unwired navigation hyperlinks across all six screens, and duplicated conditional formatting rules on the Home dashboard.
2. **RC2 Independent QA Verification** — an adversarial review that deliberately tested incomplete/careless input rather than correct input. Found and fixed two additional bugs: a blank Due Date on Bills or Clients incorrectly produced a false "Overdue" status, and a blank Money Direction on Quick Add silently corrupted a staged transaction's calculation contribution.

Both audit cycles are documented in full, including every test scenario run and its result, in the technical documentation.

## Known Limitations

This release is fully functional but has four documented, intentional limitations — none are bugs, all were architectural decisions made and recorded during development:

1. **Manual staging workflow.** Adding a transaction, bill, invoice, or goal requires copying a computed "staging row" and pasting it as values into the appropriate hidden table. Native Excel formulas cannot write and reset themselves; removing this step requires VBA or Office Scripts, which this release deliberately does not include.
2. **Static currency symbol.** The Currency setting is stored and used correctly throughout the calculation engines, but every dollar amount on screen uses a hardcoded `$` — changing Currency does not change the displayed symbol.
3. **Partial Business Health scoring.** Two of five Business Health components (Cash Flow, Activity) are fully active. Three (Cash Runway, Bills, Invoices) exist as clearly labeled, architecturally-reserved placeholders — real data exists for Bills and Invoices, but activating their score contribution requires either extending `_calc_Core` or relaxing `_calc_Health`'s single-source-of-truth restriction, both deliberately deferred to a future release.
4. **Single active goal visibility.** The Insights engine surfaces only the highest-priority Active goal; a second active goal is not currently mentioned.

## Upgrade Notes

This is the initial release — no upgrade path applies.

## System Requirements

- Microsoft Excel 365 or Excel 2021+ (desktop). Core functionality is expected to work in Excel Online and Excel Mobile, though the staging/copy workflow is easiest on desktop.
- No add-ins, no internet connection, and no account required — the workbook is fully self-contained.
