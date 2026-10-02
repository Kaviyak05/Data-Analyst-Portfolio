# Day 2: Data Cleaning (Superstore)

## 1. Starting point
9,994 rows (order lines) and 19 columns. The original data stays untouched on the "Raw" sheet, and all cleaning was done on "Working".

## 2. Checks and fixes

| Check | Result | Action |
| Exact duplicate rows | 1 found (same order, product, quantity and sales). Row ID was excluded from the comparison, because it is unique on every row. | Removed. 9,993 rows remain. |
| Blank cells | 0 (checked with "COUNTBLANK") | None needed |
| Garbled characters in Product Name | Broken quote marks and stray "Â" from a text encoding error | Replaced with straight quotes, and the stray "Â" removed. Searches for the leftover characters found nothing. |
| Extra spaces in Product Name | None (checked with "LEN" vs "TRIM") | None needed |
| Dates | 4,042 Order Dates were real dates with day and month swapped. 5,951 were text. | Built corrected date columns for Order Date and Ship Date |

## 3. How I validated the dates
- The largest "day" among the real dates was 12, which showed that they were read in the wrong order.
- After the fix, all 9,993 corrected dates are real dates.
- Days to Ship now ranges from 0 to 7. The 0-day rows are all Same Day shipments.

## 4. Effect on earlier findings
- Total Sales dropped by 281.37 (the removed duplicate), to 2,296,919.49.
- East order lines went from 2,848 to 2,847.
- Fixing the dates and text did not change any Day 1 number, because none of them use those columns.

## 5. One thing that confused me, and how I resolved it
- Why excel read the date in wrong format and found that how excel works (read system regional date format) whereas file date format was in US date format
