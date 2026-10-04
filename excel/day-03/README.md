# Day 3: Lookups, Logic and Discount Analysis (Superstore)

## 1. What I learned
- Lookups: "XLOOKUP" (with a "not found" message) and "INDEX/MATCH". Both returned the same manager for every row. "INDEX/MATCH" works in all Excel versions, and "XLOOKUP" is simpler.
- Logic: "IFS" to build a "Discount Band" column, and "IF" with "AND" to build a "Priority" column.
- Conditional summaries: "AVERAGEIFS", "COUNTIFS" and "SUMIF".

## 2. What I built
- "Lookups" sheet: a small Region and Manager table, joined to the data with "XLOOKUP".
- "Discount Band": None (0), Low (up to 0.2), Medium (up to 0.5), High (above 0.5).
- "Priority": "Review" when Sales is over 500 and Profit is negative, otherwise "Ok".

## 3. Finding: discounts and losses

| Discount band | Order lines | Average Profit | Total Profit |
|---|---|---|---|
| None | 4,798 | 66.90 | 320,988 |
| Low | 3,803 | 26.50 | 100,785 |
| Medium | 536 | -109.71 | -58,805 |
| High | 856 | -89.44 | -76,559 |

- In the Medium band, 491 of 536 order lines lose money (about 92%). In the High band, all 856 do.
- Medium and High are about 14% of order lines, and together they lose about 135,000.
- This shows that big discounts and losses go together. The data has no product costs, so it cannot prove that the discount caused the losses.

## 4. Checks I ran
- The four band counts add up to 9,993, which matches the table.
- The four band profit totals add up to the Total Profit.

## 5. One thing that confused me, and how I resolved it
- What confused you: why "<0" needs quotes in COUNTIFS, when [@Profit]<0 in an IF formula has none.
- How you resolved it: COUNTIFS reads the criteria as a small piece of text and splits it into the comparison sign and the number. IF evaluates the comparison directly.
