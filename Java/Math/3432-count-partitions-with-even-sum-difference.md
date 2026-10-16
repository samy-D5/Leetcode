# 3432. Count Partitions with Even Sum Difference

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-partitions-with-even-sum-difference/
**Tags:** Array, Math, Prefix Sum

## Approach 1 — 2025-12-11 23:46 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.6 MB*

```java
class Solution {
    public int countPartitions(int[] nums) {
        int total=0;
        for(int i=0; i<nums.length; i++) total += nums[i];

        int left=0 , count=0;

        for(int i=0; i<nums.length-1; i++){
            left+= nums[i];
            int right= total-left;
            if((left%2)==(right%2)) count++;
        }
        return count;
    }
}
```
