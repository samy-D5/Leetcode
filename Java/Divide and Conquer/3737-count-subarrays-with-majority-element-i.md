# 3737. Count Subarrays With Majority Element I

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/count-subarrays-with-majority-element-i/
**Tags:** Array, Hash Table, Divide and Conquer, Segment Tree, Merge Sort, Counting, Prefix Sum

## Approach 1 — 2025-11-08 20:36 (java)

*Runtime: 51 ms (faster than 11.0%) · Memory: 46.9 MB*

```java
class Solution {
    public int countMajoritySubarrays(int[] nums, int target) {
        int count =0;
        for(int i=0; i<nums.length; i++){
            int cnt=0,len=0;
            for(int j=i; j<nums.length; j++){
                
                    if(nums[j]==target) cnt++;
                    len++;
                if(cnt>len/2) count++;
            }
        }
        return count;
    }
}
```
