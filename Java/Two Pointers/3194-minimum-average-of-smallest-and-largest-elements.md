# 3194. Minimum Average of Smallest and Largest Elements

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-average-of-smallest-and-largest-elements/
**Tags:** Array, Two Pointers, Sorting

## Approach 1 — 2024-06-23 09:22 (java)

*Runtime: 2 ms (faster than 97.2%) · Memory: 43.9 MB*

```java
class Solution {
    public double minimumAverage(int[] nums) {
        Arrays.sort(nums);
        int min=0,max=nums.length-1;
        double avg=Double.MAX_VALUE;
        for(int i=0;i<nums.length/2;i++){
            double curr=(nums[max--]+nums[min++])/2.0;
            avg=Math.min(avg,curr);
        }
        return avg;
    }
}
```
