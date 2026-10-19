# 2089. Find Target Indices After Sorting Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-target-indices-after-sorting-array/
**Tags:** Array, Binary Search, Sorting

## Approach 1 — 2026-10-20 01:24 (java)

*Runtime: 6 ms (faster than 28.1%) · Memory: 49.9 MB · Time to solve: 14m 54s (timer)*

```java
class Solution {
    public List<Integer> targetIndices(int[] nums, int target) {
        List<Integer> list = new ArrayList<>();
        Arrays.sort(nums);
        for(int i=0; i<nums.length; i++){
            if(nums[i]==target) list.add(i);
        }
        return list;
    }
}
```
