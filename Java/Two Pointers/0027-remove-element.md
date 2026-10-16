# 27. Remove Element

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/remove-element/
**Tags:** Array, Two Pointers

## Approach 1 — 2024-08-08 00:46 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42 MB*

```java
class Solution {
    public int removeElement(int[] nums, int val) {
        int index=0;
        for (int i= 0; i<nums.length; i++) {
            if (nums[i]!= val) {
                nums[index]= nums[i];
                index++;
            }
        }
        return index;
    }
}
```
