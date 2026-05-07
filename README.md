# Medicare Provider Billing and Quality Performance Analysis

**Domain:** Healthcare │ **Tools:** SQL · Excel · Power BI · DAX

## Background

Medicare reimbursement rates vary significantly across specialties,
geographic regions, and individual providers.

## Objective

- Which specialties show the largest gap between submitted and allowed amounts?
- Which procedure codes represent the highest Medicare spend?
- Which individual providers are statistical outliers within their specialty?
- How does Medicare payment rate vary geographically?
- How is Medicare spend distributed across providers — is it concentrated at the top or broadly spread?

## Data

CMS Medicare Physician & Other Practitioners PUF, 2023.
Filtered to 10 states. ~4.6 million provider records. See data/README.md.

## Tools & Methodology

SQL (SQLite via DBeaver): extracted, filtered, and aggregated raw provider records.
Excel: pivot dashboard and KPI summary panel built from pre-aggregated CSV exports.
Power BI: interactive 4-page report with DAX measures, slicers, and drill-throughs.

## Key Findings

- [SPECIALTY] submitted charges averaged [X]x Medicare-allowed amounts
- [X] providers flagged as outliers at 2+ standard deviations above specialty average
- [STATE] showed the highest average Medicare payment
- Top [X] procedure codes account for 50% of total Medicare spend (Pareto)
- Top 10% of providers account for [X]% of total spend

## Recommendations

1. [SPECIALTY] warrants priority billing audit review
2. [STATES] show geographic payment variation warranting further investigation
3. Audit resources should target the top [X]% of providers, which account for [X]% of total spend — broad-based review generates noise with low ROI

## Dashboard

![Overview](images/dashboard_overview.png)
[View live Power BI report](your-powerbi-service-link)

## Analytical Limitations

[Add domain constraint notes here — see data/README.md for the full list.]

## What I Would Do Next

Join with CMS quality metrics to test whether high-billing providers correlate with
better or worse patient outcomes across the same specialties. Extend the geographic
analysis to include county-level variation within each state.
