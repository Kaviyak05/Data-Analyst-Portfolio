# Day 1: Excel Foundations (Superstore)

## 1. Dataset
Sample Superstore dataset from Kaggle: 9,994 rows and 19 columns.
One row is one **order line**, meaning one product within an order.
There are 5,009 unique orders.

## 2. What I did
- Kept the original data untouched on a "Raw" sheet and worked on a copy called "Working".
- Converted the data to an Excel Table (SalesTbl) and froze the header row.
- Used sort and filter to answer questions, and recorded the answers in "Findings".
- Wrote formulas with table references: SUM, AVERAGE, SUMIF, COUNTIF.
- Added two calculated columns: Profit Margin and Order Size.
- Built a Region × Category sales grid with one SUMIFS formula, using mixed references ($A25, B$24).

## 3. Findings (before cleaning)
- Total Sales is 2,297,200.86 and Total Profit is 286,397.02. The average Discount is about 15.6%.
- There are 595 unique Furniture orders in the West region (707 order lines).
- 1,871 order lines have negative Profit.

## 4. Data issues
**Found:**
- Order Date and Ship Date are in mixed formats. Some are real dates with day and month swapped, and some are text.
- Some product names contain garbled characters.

**Not checked yet (planned for Day 2 cleaning):**
- Exact duplicate rows
- Blank values

## 5. One thing that confused me
- Got to know the difference bwtween column name with table name and @<column_name> in tables
- And formulas (SUMIF,COUNTIF)
