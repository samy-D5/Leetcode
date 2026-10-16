# 442. Find All Duplicates in an Array

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/find-all-duplicates-in-an-array/
**Tags:** Array, Hash Table, Sorting

## Approach 1 — 2024-12-22 21:58 (java)

*Runtime: 5 ms (faster than 95.4%) · Memory: 53.1 MB*

```java
class Solution {
    public List<Integer> findDuplicates(int[] nums) {
        List<Integer> ans=new ArrayList<>();
        for(int i=0;i<nums.length;i++){
            int count=Math.abs(nums[i]);
            if(nums[count-1]<0) ans.add(count);
            nums[count-1]*=-1;
        }
        return ans;
    }
}
```
