# Changelog

All notable changes to Business Finance Pro are documented in this file.

## [1.0.2] — Navigation fix

### Fixed
- **Navigation buttons did not work.** The nav bar links (Home, Quick Add, Bills, Clients, Goals, Insights) were stored as links to external files, so clicking one showed an Excel security warning and a path like `C:\Users\...\Home!A1` instead of switching screens. All 36 nav links across the six screens are now internal workbook links.
- The **Insights** button used to go to Home; it now jumps to the "This week" insights section on the Home screen.

### Tested
- Recalculated with 0 formula errors; no other cell values changed.

---

## [1.0.1] — Bug-fix release

### Fixed
- **Overdue/Upcoming status was frozen after saving a record.** Status was computed with `TODAY()` only in the staging row, so once the row was pasted as values it never updated (a bill due months ago still showed "Upcoming"). The Bills and Clients screens and the Needs Attention engine now calculate status live from the due date. The only status you set by hand is `Paid` (and `Void`/`Draft` for invoices).
- **Overdue counts and totals** on the Home dashboard (`_calc_Attention`) now use the live status, with guards for blank due dates and Paid/Void/Draft records.
- **Sample data went stale.** Sample transactions, bills, invoices and goal dates were fixed July 2026 dates, so the dashboard opened as "Getting started / $0" in any later month. Sample dates are now relative to today. Delete the sample rows before entering real data.
- **Quick Add example did not link to its customer.** The example client was typed "Blue Harbor Café" (accent) but stored as "Blue Harbor Cafe", so the CustomerID came out blank. Fixed the example, and the Vendor / client dropdown now lists customers as well as vendors (new named range `PayeeNameList`).

### Changed
- Two more sample transactions added so the Home dashboard shows Money In, Money Out and a health rating on first open.
- Version string in Settings updated to 1.0.1. Named ranges: 106 -> 107.

### Tested
- Recalculated with 0 formula errors. Re-tested: stale "Upcoming" bill with a past due date now shows Overdue; Paid bills and Draft/Paid invoices are not counted as overdue; a blank due date is not flagged overdue; staging row links a customer and a vendor correctly.

---

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