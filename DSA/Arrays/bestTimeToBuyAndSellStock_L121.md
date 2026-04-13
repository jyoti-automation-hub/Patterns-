## 💻 Max Profit (Best Time to Buy and Sell Stock)

```java
class Solution {
    public int maxProfit(int[] prices) {

        int minPrice = Integer.MAX_VALUE;
        int maxProfit = 0;

        for (int price : prices) {

            if (price < minPrice) {
                minPrice = price;
            }

            int profit = price - minPrice;

            if (profit > maxProfit) {
                maxProfit = profit;
            }
        }

        return maxProfit;
    }
}

```
---

####  👉 “Track lowest price so far, and at each step calculate profit if sold today.”

👉 minPrice  
- The lowest price seen so far  
- Meaning → best day to buy  

👉 price[i] (current price)  
- Price on current day  
- Meaning → potential day to sell

---
## 🧠 Formula

profit = current price - minPrice

👉 Translation:
- Buy at cheapest earlier price (minPrice)  
- Sell today (price[i])

---
