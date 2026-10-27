# Bus Fare Optimizer

A DAA (Design and Analysis of Algorithms) mini project that finds the cheapest way to buy bus tickets using Dynamic Programming.

## Problem
You are given the price of a single ticket, a day pass and a weekly pass (valid for 7 days in a row), and the number of trips you take each day. Find the cheapest way to cover all the days.

## Approach
Let `dp[i]` be the minimum cost to cover the first `i` days.

```
dp[i] = min( dp[i-1] + min(trips[i] * single, dayPass),
             dp[max(0, i-7)] + weeklyPass )
```

The answer is `dp[n]`. To find what to buy, we walk backwards from day `n` using the stored choices.

## Complexity
- Time: O(n)
- Space: O(n)

where `n` is the number of days.

## How to run
Open `index.html` in any web browser. No installation needed.

## Technologies
HTML and JavaScript only.

## Sample input
- Single: 20, Day pass: 70, Weekly pass: 250
- Trips per day: `2,3,0,4,5,1,0,2,6,4,3,0,5,2`
