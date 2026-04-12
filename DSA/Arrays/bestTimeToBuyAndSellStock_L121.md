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

### [7, 1, 4]

### Initialization
- minPrice = ∞  
- maxProfit = 0  

---

### Iteration 1 (price = 7)
- minPrice = min(∞, 7) = 7  
- profit = 7 - 7 = 0  
- maxProfit = 0  

---

### Iteration 2 (price = 1)
- minPrice = min(7, 1) = 1  
- profit = 1 - 1 = 0  
- maxProfit = 0  

---

### Iteration 3 (price = 4)
- minPrice = 1  
- profit = 4 - 1 = 3  
- maxProfit = 3  

---

### ✅ Final Output
3

---

