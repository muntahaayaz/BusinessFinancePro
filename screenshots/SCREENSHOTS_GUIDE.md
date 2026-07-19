# Screenshots Guide

Capture these in order — this sequence tells the product's story from first open to daily use, and doubles as the natural order for a portfolio case study or README gallery.

## Before You Start

- Use the seed data already in the workbook (Riverside Design Studio / Blue Harbor Cafe / City Wholesale Supplies) — it's realistic and consistent across every screen, so screenshots taken at different times still look like one coherent product.
- Set Excel zoom to 100%, window width wide enough that no horizontal scroll bar appears.
- Hide the Excel ribbon (Ctrl+F1) and formula bar (View tab > uncheck Formula Bar) before capturing — this is what makes the product look like software, not a spreadsheet.
- Confirm gridlines and row/column headers are off (they should be, by default, on every visible sheet).

## Shot List

1. **Home Dashboard — full screen.** The hero shot. Should show the Business Health card, Money In/Out, Needs Attention (with at least one item populated), and the Monday Briefing narrative all visible together. This is the single image most likely to appear first in any portfolio or README.

2. **Home Dashboard — Business Health close-up.** A tight crop on just the health card. Useful for illustrating the "plain language, no numbers" design decision on its own.

3. **Settings — Business Information section.** Shows the guided setup fields (Business name, Industry, Currency, Fiscal year start).

4. **Settings — full screen.** All four sections (Business Information, Appearance, Preferences, Product Information) visible in one shot.

5. **Quick Add — empty state.** The "What happened?" card with no input yet — shows the clean entry form itself.

6. **Quick Add — filled in, staging row visible.** Same screen with all seven fields completed and the "Ready to save" staging row showing computed values. This is the shot to use if you need to explain the staging workflow in a case study.

7. **Bills — list card with both an upcoming and an overdue bill visible.** The color contrast between statuses should be visible in this shot.

8. **Clients — invoice list, same treatment as Bills.**

9. **Goals — list card showing the progress display** (e.g., "$5,580 of $9,000 (62%)").

10. **Navigation in motion (optional, for a GIF/video instead of a static shot).** Click through Home → Quick Add → Bills → Clients → Goals in sequence to show the hyperlink navigation working.

## Optional / Advanced

11. **Hidden sheet structure** (Developer tab visible, sheet tabs unhidden) — only include this in a technical case study aimed at other Excel developers, not in a customer-facing gallery. It's the "how it's built" shot, not the "what it looks like" shot.

12. **A formula bar close-up** of one of the calculation engine sheets (e.g., `_calc_Health`'s Section 3) — useful only for a technical audience wanting to see the underlying rule logic.

## Naming Convention

```
01-home-dashboard-full.png
02-home-business-health.png
03-settings-business-info.png
04-settings-full.png
05-quickadd-empty.png
06-quickadd-filled-staging.png
07-bills-list.png
08-clients-list.png
09-goals-list.png
10-navigation-demo.gif
```

Numbered prefixes keep them in narrative order in any file browser or gallery, independent of capture date.
