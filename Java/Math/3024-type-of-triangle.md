# 3024. Type of Triangle

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/type-of-triangle/
**Tags:** Array, Math, Sorting, Polygons

## Approach 1 — 2024-06-25 12:29 (java)

*Runtime: 1 ms (faster than 55.7%) · Memory: 41.9 MB*

```java
class Solution {
    public String triangleType(int[] nums) {
       int ans1=nums[0]+nums[1];
       int ans2=nums[1]+nums[2];
       int ans3=nums[0]+nums[2];
       if(ans1<=nums[2] || ans2<=nums[0] || ans3<=nums[1]) return "none";
       if(nums[0]==nums[1] && nums[1]==nums[2]) return "equilateral";
       if(nums[0]==nums[1] || nums[1]==nums[2] || nums[0]==nums[2]) return "isosceles"; 
       return "scalene";
    }
}
```
