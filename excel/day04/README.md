
# Day 4: PivotTables and Slicers (Superstore)

## 1. What I learned
- PivotTables work like SQL "GROUP BY": Rows are the grouping column, Values are "SUM", "AVG" or "COUNT", Columns add a second grouping, and Filters work like "WHERE".
- Slicers are buttons that filter a PivotTable by one or more values, such as Region.
- A PivotTable must be refreshed when the data changes. Sorting applies to the column you click in.

## 2. What I built
- A discount-band PivotTable (total profit, order lines, average profit), with Region as a second grouping and a Region slicer.
- A category PivotTable with sales and profit, and a category-by-discount-band profit table.
- A sales-by-year PivotTable, using the cleaned date column from Day 2.

## 3. Findings

**Discount bands.** The PivotTable matched my Day 3 formulas exactly.
- None and Low earn money. Medium and High lose money, in every region.

**Categories.**

| Category | Sales | Profit | Margin |
|---|---|---|---|
| Technology | 836,154 | 145,455 | 17.4% |
| Furniture | 741,718 | 18,463 | 2.5% |
| Office Supplies | 719,047 | 122,491 | 17.0% |

- Furniture sells more than Office Supplies but earns far less. Its Medium discount band loses about 44,626.
- Office Supplies has no Medium-band rows. Only its High band loses money (about 47,140), and the category still earns 122,491.
- In Technology, the High band loses the most (about 19,579), and the category still earns 145,455.

**Sales over time.**
- Sales dipped slightly from 483,966 in 2014 to 470,533 in 2015, then rose to 609,206 in 2016 and 733,215 in 2017.
- 2017 sales are about 56% above 2015.

## 4. Checks I ran
- Every PivotTable Grand Total matched my earlier totals (Sales 2,296,919.49 and Profit 286,409.08).
- The slicer combined two regions correctly (Medium order lines: 205 + 39 = 244).
- An empty PivotTable cell means no rows for that combination. It is not the same as 0.

## 5. One thing that confused me, and how I resolved it
I was confused about how percentages work, and how to tell what a percentage is a percentage *of*. I moved on before I fully understood it. What I understand now: a percentage is a part divided by a whole, and growth is the increase divided by the starting value. For example, 491 of 536 Medium rows lose money (about 92%), and sales rising from 100 to 150 is 50% growth.

What I still want to practise: how percentages work, how to find the right percentage for a question, and how to explain the result in words.
