# 3010. Divide an Array Into Subarrays With Minimum Cost I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/divide-an-array-into-subarrays-with-minimum-cost-i/
**Tags:** Array, Sorting, Enumeration

## Approach 1 — 2026-02-26 23:17 (java)

*Runtime: 1 ms (faster than 98.4%) · Memory: 45.4 MB*

```java
class Solution {
    public int minimumCost(int[] nums) {
        int n=nums.length;
        int a=Integer.MAX_VALUE;
        int b=Integer.MAX_VALUE;

        for(int i=1; i<n; i++){
            if(nums[i]<a){
                b=a;
                a=nums[i];
            }else if(nums[i]<b){
                b=nums[i];
            }
        }
        return nums[0]+a+b;
    }
}
```
