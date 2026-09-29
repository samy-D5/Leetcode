# 561. Array Partition

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/array-partition/
**Tags:** Array, Greedy, Sorting, Counting Sort

## Approach 1 — 2026-09-29 20:35 (java)

*Runtime: 18 ms (faster than 31.0%) · Memory: 49.6 MB*

```java
class Solution {
    public int arrayPairSum(int[] nums) {
        Arrays.sort(nums);
        int i=0,sum=0;
        while(i<nums.length){
            sum+=Math.min(nums[i],nums[i+1]);
            i+=2;
        }
        return sum;
    }
}
```
