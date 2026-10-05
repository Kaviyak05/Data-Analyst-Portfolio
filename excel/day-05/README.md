# Day 5: Charts and Dashboard (Superstore)

## 1. What I learned
- Choose the chart for the question: a line for change over time, a column chart for comparing categories. A pie chart can't show negative values, so it doesn't suit profit by discount band.
- A chart should make its point without help: a clear title, a unit on the axis, a legend only when there is more than one series, and one measure per chart.
- A slicer only filters the PivotTables it is connected to. I connected the Region slicer to all three.
- The number grouping on an axis, such as $8,00,000, follows the system's regional setting.

## 2. What I built
A one-page "Dashboard" sheet with:
- Total profit by discount band (column chart)
- Sales and profit by category (column chart)
- Total sales by year (line chart)
- A Region slicer that filters all three charts, a headline with the main finding, and a caption under each chart

## 3. Findings
- Medium and High discount bands lose money. None and Low earn it.
- Furniture sells nearly as much as the other categories but earns the least profit.
- Sales dipped slightly in 2015, then rose each year to 2017.
- These charts show that discounts and losses go together. They do not prove that discounts caused the losses.

## 4. Improvements I made along the way
- Removed the legend and field buttons from single-series charts.
- Dropped Order lines and Average of profit from the discount chart, because they were on a different scale and almost invisible.
- Moved the axis labels to the bottom so they did not sit on the negative bars.
- Hid the grid lines and fitted all three charts on one screen.

## 5. One thing that confused me, and how I resolved it
- Structuring the findings , and how i resolved it checked existing excel dashboard on online and added the finding in my dashboar.
