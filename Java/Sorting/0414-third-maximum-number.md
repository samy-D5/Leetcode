# 414. Third Maximum Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/third-maximum-number/
**Tags:** Array, Sorting

## Approach 1 — 2025-12-06 00:07 (java)

*Runtime: 4 ms (faster than 44.7%) · Memory: 44.7 MB*

```java
class Solution {
        public int thirdMax(int[] nums) {
        Integer max1 = null;
        Integer max2 = null;
        Integer max3 = null;
        for (Integer n : nums) {
            if (n.equals(max1) || n.equals(max2) || n.equals(max3)) continue;
            if (max1 == null || n > max1) {
                max3 = max2;
                max2 = max1;
                max1 = n;
            } else if (max2 == null || n > max2) {
                max3 = max2;
                max2 = n;
            } else if (max3 == null || n > max3) {
                max3 = n;
            }
        }
        return max3 == null ? max1 : max3;
    }
}
```
