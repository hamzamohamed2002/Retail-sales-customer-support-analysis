# Retail Sales & Customer Support Dashboard

## Overview
An interactive Excel dashboard that analyzes the sales performance of a retail company selling in 8 countries through two channels (In Store and Online), and links it to cancellations, returns, and customer satisfaction with support.

- Period: January 2022 – December 2024
- Size: 5,200 orders and 1,327 support tickets (after cleaning)
- Dataset: a deliberately messy retail dataset (orders table and support tickets table), source not recorded

## Dashboard
![Retail Sales & Customer Support Dashboard](dashboard.JPG)

## Data Cleaning (Power Query)
Main problems fixed:
- 24 different spellings of 8 countries
- Dates in several text formats
- Quantity written as text (such as "two" and "N/A")
- Several order statuses meaning the same thing
- An out-of-range CSAT score (6)
- Negative resolution times
- Blank and duplicate rows

All 31 cleaning steps are documented in the Cleaning Logs sheet.

Verification: net revenue by country and net revenue by category give the same total (2,554,354), and no ticket is left without a matching order.

## Key Metrics
- Net Revenue: 2,554,354
- Avg CSAT Score: 3.83 / 5
- Cancellation Rate: 12.0% (625 of 5,200 orders)
- Return Rate: 7.8% (407 of 5,200 orders)
- Orders with tickets: 22.4% (1,163 of 5,200 orders)

Net Revenue = Quantity x Unit Price x (1 - Discount), for Delivered and In Progress orders, excluding shipping.

## Key Findings
1. Revenue is evenly spread: the 8 countries range from 302,219 (UAE) to 330,285 (Saudi Arabia), and categories from 391,563 (Toys) to 449,631 (Beauty).
2. In Store brings 55.8% of net revenue vs 44.2% for Online.
3. Delivery Delay is the top ticket driver (178 of 1,327 tickets, 13.4%), and it is also the second lowest in satisfaction (CSAT 3.72). Product Defect has the lowest CSAT (3.63).
4. Priority does not change resolution time: Low 48.7 hours, Medium 48.1, High 47.4, Urgent 48.6.
5. The cancellation rate is stable around 12% every year (12.4% in 2022, 11.5% in 2023, 12.3% in 2024), with a peak in February in 2023 and 2024.
6. Revenue in 2024 (859,437) is higher than 2023 (815,960), about +5.3%.

## Limitations
- 300 orders have no quantity in the raw data, so they have no revenue (249 of them are Delivered or In Progress, so net revenue is slightly understated).
- 100 orders have no valid date, so they count in the KPI cards but not in the year and month charts.
- 165 tickets have no CSAT score. The average is calculated on the 1,162 rated tickets.
- Net Revenue includes In Progress orders. Using Delivered only gives a more conservative figure.
- Cleaning relied on assumptions, such as treating Shipped, In Transit, and Processing as In Progress.

## Tools
Excel (Power Query, Data Model, DAX, PivotTables, PivotCharts, Slicers)

## Contact
LinkedIn: https://www.linkedin.com/in/hamza-yosry
