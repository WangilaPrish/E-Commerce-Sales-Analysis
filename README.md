# E-Commerce Sales Analytics (Power BI)
> Status: work in progress

## Goal
Find where sales rise but profit doesn't, using 138K orders (2021-2025).

## Data
Kaggle "E-Commerce Sales Analytics Dataset" (CC0, simulated data).
Files not included; download from Kaggle.

## Data quality findings
- Flat file omits items for 11,226 orders (8%) vs order_items.
- `net_sales` includes tax and shipping.
- Cancelled/pending/returned orders still carry sales and profit.
- `currency` labels are not backed by converted values.
- Delivery days and ratings are empty for non-completed orders.

## Modelling decisions
- Star schema: order_items (fact); orders, products, customers, Date.
- All KPIs count Completed orders only.
- Net Revenue = gross sales - discounts (before tax and shipping).

## Progress
- [x] Data profiling and cleaning
- [x] Data model and relationships
- [ ] Executive overview page
- [ ] Sales vs profit
- [ ] Customers and RFM
- [ ] Logistics and returns
