# Fresh Cart Grocery Performance Dashboard

Excel dashboard for monitoring grocery sales, customer activity and delivery operations.

## Project description

Analyzed 900 cleaned grocery orders and built an interactive Excel dashboard covering revenue, delivered orders, customer reach, delivery speed, customer ratings and product/category performance.

## Business problem

Grocery teams need consistent measures of realized sales and service quality. Order cancellations, varied text labels and missing delivery information can distort reporting. This project separates raw data, standardized records, calculations and dashboard reporting.

## Dashboard KPIs

| Measure | Current workbook result |
|---|---:|
| Net revenue | 310,860.65 |
| Total orders | 900 |
| Delivered orders | 834 |
| Unique delivered customers | 284 |
| Average order value | 372.73 |
| Average delivery time | 24.31 minutes |
| On-time delivery rate | 75.06% |
| Delivery success rate | 92.67% |
| Average rating | 4.25 / 5 |

Currency is not specified. Figures represent the dashboard's currently selected full period, all zones and categories.

## Workbook structure

- **Dashboard:** interactive KPI reporting with start/end dates, zone and category filters.
- **Analysis:** KPI calculations, revenue summaries and product/category rankings.
- **Customers:** customer-level counts and active-customer measures.
- **Settings:** selectable filters and lookup values.
- **Clean:** 900 standardized records with calculated sales and time fields.
- **Raw:** source order data before cleaning.
- **Audit:** reconciliation and validation checks.

## Data dictionary

| Column | Definition |
|---|---|
| `OrderID` | Unique order identifier; validate uniqueness. |
| `OrderDate` | Date of order; stored as an Excel date serial. |
| `OrderHour` | Hour of the day the order was placed. |
| `CustomerID` | Customer identifier; pseudonymous but still potentially linkable. |
| `CustomerType` | Customer segment, e.g. Returning. |
| `Zone` | Delivery area; standardized in the Clean sheet. |
| `Category` | Grocery product category. |
| `Product` | Product purchased. |
| `Quantity` | Number of units ordered. |
| `UnitPrice` | Price per unit before discount; currency not specified. |
| `DiscountPct` | Discount rate as decimal, e.g. 0.10 = 10%. |
| `Status` | Order outcome, e.g. Delivered or Cancelled. |
| `DeliveryMinutes` | Recorded delivery duration; blank for some undelivered orders. |
| `FulfilmentMinutes` | Recorded order preparation/fulfilment duration. |
| `Rating` | Customer rating where available. |
| `GrossSales` | Quantity × UnitPrice. |
| `DiscountAmount` | GrossSales × DiscountPct. |
| `NetRevenue` | Realized order revenue after discounts and status rules; cancelled orders may be zero. |
| `TimeBand` | Derived grouping of order hour, e.g. Afternoon. |
| `Weekday` | Derived abbreviated day name. |
| `WeekdayNo` | Numeric weekday sort order. |
| `TimeBandNo` | Numeric time-band sort order. |

## Key calculations

- **Gross sales:** `Quantity * UnitPrice`
- **Discount amount:** `GrossSales * DiscountPct`
- **Net revenue:** realized revenue after applicable discounts and status rules
- **Delivery success rate:** `Delivered orders / Total orders * 100`
- **Average order value:** `Net revenue / Delivered orders`
- **Unique delivered customers:** distinct customer IDs among delivered orders

## Questions explored

How do products, categories, zones, weekdays and time bands affect revenue and order volume? Where do delivery performance and customer experience vary?

## Limitations

The workbook does not identify the currency, data provenance or publication licence. The raw and clean row counts differ; inspect the Audit sheet and cleaning logic before claiming complete source coverage. Ratings and delivery durations can be missing for cancelled orders. On-time criteria should be checked in workbook formulas. Net revenue is not profit.

## Dashboard Preview

### 1. Summary Dashboard

##[Grocery PerformanceDashboard]<img width="2571" height="2882" alt="Dashboard_Preview" src="https://github.com/user-attachments/assets/42a8167a-e5f5-467d-8d8b-6a8caf58ea3f" />

## Repository contents

- `Grocery_Performance_Dashboard(1).xlsx` — Excel workbook
- `Grocery_Project_Documentation.pdf` — project problem statement, terminology and KPI definitions
- `README.md` — repository overview

## Tools

Microsoft Excel, formulas, interactive filters, data cleaning, KPI reporting and validation.

