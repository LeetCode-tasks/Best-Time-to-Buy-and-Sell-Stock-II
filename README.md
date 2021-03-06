# Best Time to Buy and Sell Stock II

You are given an array prices where prices[i] is the price of a given stock on the ith day.

Find the maximum profit you can achieve. You may complete as many transactions as you like (i.e., buy one and sell one share of the stock multiple times).

**Note:** You may not engage in multiple transactions simultaneously (i.e., you must sell the stock before you buy again).

### Example:

**_Input:_** `prices = [7,1,5,3,6,4]`

**_Output:_** `7`

**_Explanation:_** Buy on day 2 (price = 1) and sell on day 3 (price = 5), profit = 5-1 = 4.
Then buy on day 4 (price = 3) and sell on day 5 (price = 6), profit = 6-3 = 3.

### Constraints:

`1 <= prices.length <= 3 * 10^4`

`0 <= prices[i] <= 10^4`

## Solution in JavaScript:

```
var maxProfit = function(prices) {
    let maxprofit = 0;
    
    for (let i = 1; i < prices.length; i++) {
        if (prices[i] > prices[i - 1]) {
            maxprofit += prices[i] - prices[i - 1];
        }
    }
    return maxprofit;
};
```
