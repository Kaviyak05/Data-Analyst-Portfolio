
# Day 7: Correlation and What-If Analysis (Superstore)

## 1. What I learned
- Correlation ("CORREL") is a number from -1 to +1 that shows how strongly two columns move together. It shows that two things move together, but not why.
- A what-if analysis changes one input and shows what happens to the result.
- Goal Seek works backwards: I set the result I want ("C2"), and Excel changes one input cell ("B2") to reach it. The input cell must hold a typed number, not a formula.
- A percentage is part ÷ whole. Subtract first only when the thing I want to describe is a change, such as growth.

## 2. What I built
A "WhatIf" sheet with:
- A model: profit today, losses removed, profit after change, and growth
- A Goal Seek version of the same model, with a target profit of 400,000
- The correlation between Discount and Profit

## 3. Results
- **Correlation, Discount vs Profit: -0.22.** Higher discounts tend to go with lower profit, but the link is weak, and it does not show why.
- **What-if:** the Medium and High bands lose 135,364 in total. If those losses stopped, profit would rise from 286,409 to 421,773, an increase of 47.3%. This is a ceiling, because it assumes nothing else changes.
- **Goal Seek:** to reach a profit of 400,000, about 113,591 of those losses would need to be removed. That is 84% of the total loss (113,591 is 84% of 135,364).

## 4. Checks I ran
- Goal Seek's answer adds up: 286,409 + 113,591 = 400,000.
- The loss removed is entered as a positive number, because removing a loss raises profit. Entering it as negative lowers the total.
- I put the original model back after Goal Seek by retyping 135,364 in the input cell.

## 5. One thing that confused me, and how I resolved it
- **When to subtract and when only to divide.** I wrote "=B6-B2/B2" to find the share of losses removed, and it gave the wrong answer. Excel divides before it subtracts, and I didn't need a subtraction at all. The number I wanted (the loss removed) was already in a cell, so only a division was needed. 
