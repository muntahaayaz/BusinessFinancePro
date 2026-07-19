# Business Finance Pro — Branding Guide

This guide reflects the color palette and typography that were actually locked in the project's Design System and built into the workbook — nothing here is aspirational or unbuilt.

## Color Palette

| Token | Hex | Usage |
|---|---|---|
| Primary | `#1D6E56` | Brand accent, active navigation state |
| Secondary | `#0C447C` | Links, informational accents |
| Success | `#3B6D11` | Positive states, Health = Good/Excellent |
| Warning | `#854F0B` | Caution states, approaching urgency |
| Critical | `#791F1F` | Overdue items, Health = Needs Attention |
| Information | `#185FA5` | Neutral system messages |
| Background | `#F7F6F2` | Page canvas |
| Surface | `#FFFFFF` | Card backgrounds |
| Border | `#E4E2DA` | Hairline dividers |
| Text Primary | `#26211C` | Headlines, body copy |
| Text Secondary | `#5F5E5A` | Supporting labels |

## Typography

- **Primary font:** Aptos (Excel 365 default), fallback Segoe UI
- Two weights only: Regular (400) and Medium/Bold (500) — never heavier
- Sentence case everywhere — no Title Case, no ALL CAPS, including in headers and buttons

## Logo Concept

The logo mark is a simple upward-trending line inside a rounded square, rendered in Primary (`#1D6E56`) on a white or transparent background — echoing the "Good/Excellent" trend-line icon already used inside the product's own Business Health engine (`trending-up`), so the logo and the in-product iconography share a visual language rather than being invented separately.

Two variants are provided in `logo/`:
- `logo-mark.svg` — icon only, for favicons, app tiles, small placements
- `logo-wordmark.svg` — mark + "Business Finance Pro" wordmark, for headers and title slides

## Icon Style

The product's own design system specifies **outline icons only, single consistent weight, no filled variants, no emoji** — any marketing or documentation iconography should follow the same rule for visual consistency between the product and its marketing materials. `icons/favicon.svg` follows this convention.

## Voice

Warm, plain-spoken, second person, no exclamation points — the same voice used throughout the product itself (see the Home dashboard's "Needs attention" and "This week" copy for reference). Marketing copy should not sound more hyped or more technical than the product does.

## What NOT to Do

- Don't use a gradient, drop shadow, or glow anywhere — the product itself uses none
- Don't introduce a new accent color beyond the palette above
- Don't use Title Case in headlines ("Business Finance Pro helps you" not "Business Finance Pro Helps You")
- Don't use stock-photo imagery of stressed business owners or generic "finance" iconography (calculators, coins, piggy banks) — it contradicts the calm, competent-friend tone the product itself establishes
