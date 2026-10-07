# Physician Ownership & Financial Interest Analytics

A Power BI analysis of CMS Open Payments ownership data, examining the financial
relationships between physicians and healthcare manufacturers — including how
much of reported ownership value came from actual cash investment versus
equity granted as compensation.

## Overview

This project analyzes physician ownership and investment interest disclosures
from CMS's Open Payments ("Sunshine Act") dataset for Program Year 2025. It
explores ownership value, investment patterns, physician specialties,
manufacturer relationships, and the split between physician-held and
family-held interests — surfacing financial exposure patterns that go beyond
simple consulting or speaking fees.

## Dashboard

![Dashboard](screenshots/dashboard.png)

## Detailed Analysis

![Detailed Analysis](screenshots/detailed_analysis.png)

## Key Insights

- **Total ownership value:** $1.25B across all disclosed interests
- **Total reported cash investment:** $200.16M
- **True value growth ratio:** 2.29× on actual invested capital
- **2,646 ownership records** across **2,222 distinct physicians** and **228 manufacturers**
- **Nearly two-thirds (63%) of ownership value** came from equity granted as
  compensation rather than purchased with cash — a more direct financial
  alignment than simple stock ownership implies
- Ownership interests held by physicians directly vs. an immediate family
  member were analyzed separately to surface indirect disclosure patterns
- Orthopaedic Surgery and other procedural/device-heavy specialties show the
  highest concentration of ownership value

## Methodology

1. **Data cleaning (Power Query):** reduced ~30 raw columns to the ~15
   analytically relevant fields, standardized recipient identification
   (physician vs. non-physician), and handled null/blank patterns in
   investment-related fields.
2. **Modeling (DAX):** built measures to separate real cash-based returns from
   compensation-based equity value, including a corrected "true" value growth
   ratio that excludes zero-investment rows from the calculation.
3. **Visualization (Power BI):** built an overview dashboard plus a detailed
   drill-down page with full breakdowns by physician specialty, manufacturer,
   and ownership holder type.

## Analysis Performed

- Physician specialty analysis (ownership value vs. investment)
- Manufacturer analysis (top manufacturers by ownership value)
- Investment vs. ownership value comparison (real investment vs. granted equity)
- Physician-held vs. family-held ownership breakdown
- Ownership type / instrument analysis (stock, stock options, convertible notes, etc.)
- Geographic distribution of physicians by state
- Physician specialty–manufacturer relationship mapping

## Tools Used

- Power BI (data modeling, DAX, dashboard design)
- Power Query (data cleaning and transformation)
- DAX (custom measures and calculated columns)

## Dataset

**Source:** CMS Open Payments — Ownership Payment Data (Program Year 2025)
https://openpaymentsdata.cms.gov

## Limitations & Disclaimer

This analysis is for educational and portfolio purposes. It describes
patterns and financial relationships present in the reported dataset only —
it does not include prescribing data, and does not establish or imply actual
conflicts of interest, undue influence, or causality. Findings should be
read as describing *financial exposure*, not *clinical outcomes*.
