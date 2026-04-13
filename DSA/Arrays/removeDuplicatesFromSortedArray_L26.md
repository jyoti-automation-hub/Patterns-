## 💻 Remove Duplicates from Sorted Array

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        
        // Edge case
        if (nums.length == 0) return 0;

        int k = 1; // first element is always unique

        for (int j = 1; j < nums.length; j++) {
            
            // check if current element is different from previous
            if (nums[j] != nums[j - 1]) {
                
                nums[k] = nums[j]; // place unique element
                k++;               // move k forward
            }
        }

        return k; // number of unique elements
    }
}
```

---
