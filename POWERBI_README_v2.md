# Automotive Incentive Performance Dashboard

**Power BI · DAX · Data Modeling**

## The Problem

Automotive OEM incentive programs pay dealers based on hitting sales targets — but with payouts, targets, and compliance scattered across regions and manufacturers, it's hard to catch underperforming dealers or pricing/payout anomalies before an incentive period closes. By the time issues show up in monthly reporting, the payout has often already gone out.

## The Approach

Built a 3-page Power BI dashboard on incentive and sales data across 5 Canadian regions and 8 OEM manufacturers:

- Modeled a proper star schema with a dedicated Date table, enabling accurate time-based analysis rather than relying on raw date columns
- Wrote time-intelligence DAX (`DATEADD`) to calculate month-over-month payout change, and `CALCULATE` + `DISTINCTCOUNT` logic to compute a live dealer compliance rate
- Used rule-based conditional formatting to flag "At Risk" and "Non-Compliant" dealers directly in a drill-down table, rather than requiring someone to manually scan raw numbers
- Added a scatter plot comparing target vs. actual units sold, sized by payout amount, to make over/under-performing dealers visually obvious at a glance

## The Insight

The dashboard surfaces exactly which dealers are trending toward missing targets *before* the incentive period closes — turning a reactive, end-of-month reporting process into something that supports proactive intervention. The Region/OEM breakdown also makes it immediately visible which manufacturer-region combinations are consistently over or under target, which is the kind of pattern that's easy to miss in a flat spreadsheet.

## Why this project

This reflects the type of incentive auditing and compliance tracking I do as an Incentive Analyst at J.D. Power — built here on fully synthetic data so it's safe to share publicly.

---

## Files

| File | Purpose |
|------|---------|
| `Automotive_Incentive_Dataset.xlsx` | Synthetic source data (621 rows) |
| `Automotive_Incentive_Dashboard.pdf` | Full 3-page report export |

**[View the full dashboard (PDF, all 3 pages)](Automotive_Incentive_Dashboard.pdf)**

## Techniques demonstrated

Star-schema data modeling · Time-intelligence DAX (`DATEADD`) · `CALCULATE`/`DISTINCTCOUNT` for compliance metrics · Rule-based conditional formatting · Multi-page report design with drill-down structure
