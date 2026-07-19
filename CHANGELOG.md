# Changelog

All notable changes to Business Finance Pro are documented in this file.

## [1.0.0] — Macro-Free Edition

### Added
- Home Dashboard: Business Health card, Money In/Out cards, Needs Attention list, Monday Briefing narrative
- Settings screen: Business Information, Appearance, and Preferences sections, plus read-only Product Information
- Quick Add screen: 7-field guided transaction entry with computed staging row
- Bills screen: bill list with live overdue/upcoming status, add-a-bill workflow
- Clients screen: invoice list with live overdue/sent status, add-an-invoice workflow
- Goals screen: goal list with live progress display, add-a-goal workflow
- Hidden data layer: `tbl_Transactions`, `tbl_Categories`, `tbl_Vendors`, `tbl_Bills`, `tbl_Customers`, `tbl_Invoices`, `tbl_Goals`, `tbl_BusinessProfile`, `tbl_Settings` — 9 protected Excel Tables
- Four calculation engines: `_calc_Core`, `_calc_Health`, `_calc_Attention`, `_calc_Insights`
- 106 named ranges forming the data/calculation/presentation interface layer
- 16 reusable validation lists backing 46 data validation rules
- Full navigation: hyperlinked nav bar across all 6 visible screens
- Business Health weighted scoring (Cash Flow and Activity components active)
- Needs Attention rules: no transactions logged, zero income, negative cash flow, no expenses logged, overdue bills, overdue invoices
- Insights rules: biggest expense category, top vendor, income summary, average transaction size, activity level, active goal progress

### Fixed (pre-release QA)
- Navigation hyperlinks were unwired across all six visible screens — fixed during the RC1 audit
- Duplicated conditional formatting rules on the Home dashboard's Business Health card, caused by a rebuild script re-run — fixed during the RC1 audit
- Blank Due Date on the Bills or Clients staging row produced a false "Overdue" status instead of a safe blank state — fixed during the RC2 independent QA review
- Blank Money Direction on the Quick Add staging row silently corrupted the staged transaction's Money In/Out contribution — fixed during the RC2 independent QA review

### Known Limitations
See `RELEASE_NOTES_v1.0.md` and the full technical documentation for the complete, detailed list. Summary: manual staging/copy workflow for all data entry (no VBA), static currency symbol formatting, three inactive Business Health scoring components, single-goal Insight visibility.

---

*No prior versions — this is the initial release.*
