# Sales Pipeline Analytics (B2B CRM)

Analysis of about 8,800 B2B sales opportunities to answer the questions a sales operations or RevOps team asks every quarter: where the pipeline leaks, which reps and products win, and what next quarter is likely to book.

**Tools:** MySQL · Excel (Power Query, PivotTables, formulas) · Power BI (DAX)
**Status:** in progress (started November 2026)

## Business questions
1. What are the overall and per-stage conversion rates from Engaging to Won?
2. Which sales agents, managers and regional offices win the most, by value and by win rate?
3. Which products and sectors drive revenue, and where is the average deal size highest?
4. How long do deals take to close, and does cycle time differ by product or deal size?
5. What does a weighted-pipeline forecast say about the next quarter?

## Data
Source: Maven Analytics Data Playground, "CRM Sales Opportunities" (fictional B2B computer-hardware company, Oct 2016 to Dec 2017).

| Table | Rows (approx.) | Contents |
|---|---|---|
| `sales_pipeline` | 8,800 | opportunity_id, sales_agent, product, account, deal_stage, engage_date, close_date, close_value |
| `accounts` | 85 | account, sector, year_established, revenue, employees, office_location, subsidiary_of |
| `products` | 7 | product, series, sales_price |
| `sales_teams` | 35 | sales_agent, manager, regional_office |

Field definitions are in `data/raw/data_dictionary.csv`. Dates in the raw file are DD-MM-YYYY.

## Repository structure
```
data/raw/     original CSVs (unchanged)
sql/          MySQL schema and analysis queries, one business question per query
excel/        pipeline workbook and quota/capacity model
powerbi/      .pbix dashboard
images/       dashboard screenshots used below
docs/         one-page insight memo
```

## Method
1. **Load and clean** in MySQL: typed tables, date conversion, checks for nulls and orphan keys.
2. **Analyse** with SQL: conversion, win rate, deal size, cycle time, rankings (window functions).
3. **Model** in Excel: Power Query merge, pivots, rep scorecard, quota and capacity scenarios.
4. **Visualise** in Power BI: star schema, Date table, DAX measures, interactive dashboard.

## Key findings
_To be added as the analysis is completed._

## Dashboard
_Screenshots to be added in `images/`._

## Author
Snehil Suman · [LinkedIn](https://www.linkedin.com/in/snehilsuman) · [GitHub](https://github.com/bladarc-official)
