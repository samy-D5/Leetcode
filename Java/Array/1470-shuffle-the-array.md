# 1470. Shuffle the Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/shuffle-the-array/
**Tags:** Array

## Approach 1 — 2024-06-26 18:54 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.8 MB*

```java
class Solution {
    public int[] shuffle(int[] nums, int n) {
         int[] shuffled = new int[nums.length];
        int first = 0, second = n;

        for (int i = 0; i < nums.length; i++) {
            if (i % 2 == 0) 
                shuffled[i] = nums[first++];
            else 
                shuffled[i] = nums[second++];
        }
        return shuffled;
    }
}
```
