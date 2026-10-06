
# Day 6: Metrics and KPI Sheet (Superstore)

## 1. What I learned
- Most metrics follow one of four shapes: part ÷ whole, growth, average, and share of total. Every metric has a Z, the number you compare against. If I can't name the Z, I can't explain the number.
- A percentage is "X is Y% of Z". Profit margin is profit as a percentage of sales.
- Growth is (new − old) ÷ old. Putting the old value first gives the wrong sign.
- Average order value divides by the number of unique orders, not rows. Dividing by rows gives the average value of an order line, which is a different metric.
- The percent format multiplies by 100 itself, so adding "*100" to the formula shows 249% instead of 2.5%.

## 2. What I built
A "KPI" sheet with:
- Profit margin by category
- Average order value
- Sales growth, 2016 to 2017
- Share of sales by category, with a total check

## 3. Results

| Category | Sales | Profit | Margin | Share of sales |
|---|---|---|---|---|
| Technology | 836,154.03 | 145,454.95 | 17.4% | 36.4% |
| Furniture | 741,718.42 | 18,463.33 | 2.5% | 32.3% |
| Office Supplies | 719,047.03 | 122,490.80 | 17.0% | 31.3% |

- Average order value is $458.56 (total sales ÷ 5,009 unique orders).
- Sales grew 20.4% from 2016 to 2017, measured against 2016's sales.
- Furniture is about a third of sales but keeps only 2.5 cents of profit per dollar sold.

## 4. Checks I ran
- The three category shares add up to 100.0%. This check caught a Furniture formula that pointed at Office Supplies' sales.
- Average order value matches 2,296,919 ÷ 5,009.
- Dividing by the 9,993 rows instead of the orders would give about half the AOV, so the count matters.

## 5. One thing that confused me, and how I resolved it
- **The 249% margin.** I added "*100" to the profit margin formula and then applied the percent format, so the cell showed 249% instead of 2.5%. The percent format already multiplies by 100, so I removed the "*100" and kept the format.
- **The negative growth.** My growth formula gave -20% even though sales went up. I had subtracted the newer year from the older one. Putting the newer year first (new − old) fixed the sign, and the result was +20.4%.
