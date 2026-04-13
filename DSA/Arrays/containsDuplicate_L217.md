## 💻 Contains Duplicate – Full Code

```java
import java.util.HashSet;
import java.util.Set;

class Solution {
    public boolean containsDuplicate(int[] nums) {

        Set<Integer> set = new HashSet<>();

        for (int num : nums) {
            if (set.contains(num)) {
                return true;
            }
            set.add(num);
        }

        return false;
    }
}

```

---

## ❗ Important Flow

For every number:

1. Check → already seen?  
2. If YES → duplicate  
3. If NO → store it (using add)

---

## 💡 Final Understanding

- set.contains(num) → “Have I seen this before?”  
- set.add(num) → “Now remember this for future”

---
