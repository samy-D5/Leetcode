# 2057. Smallest Index With Equal Value

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/smallest-index-with-equal-value/
**Tags:** Array

## Approach 1 — 2024-06-29 15:48 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.9 MB*

```java
class Solution {
    public int smallestEqual(int[] nums) {
        //Arrays.sort(nums);
        for(int i=0;i<nums.length;i++){
            if(i%10==nums[i]) return i;
        }
        return -1;
    }
}
```
