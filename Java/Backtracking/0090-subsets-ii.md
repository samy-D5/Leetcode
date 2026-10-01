# 90. Subsets II

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/subsets-ii/
**Tags:** Array, Backtracking, Bit Manipulation

## Approach 1 — 2026-10-02 00:35 (java)

*Runtime: 2 ms (faster than 99.7%) · Memory: 45.1 MB · Time to solve: 37s*

```java
class Solution {
    public List<List<Integer>> subsetsWithDup(int[] nums) {
        List<List<Integer>> res = new ArrayList<>();
        List<Integer> subset = new ArrayList<>();
        Arrays.sort(nums);
        backtrack(0, nums, subset, res);
        return res;
    }

    private void backtrack(int i,int[]nums,List<Integer> subset,List<List<Integer>> res) {
        if(i ==nums.length){
            res.add(new ArrayList<>(subset));
            return;
        }
        subset.add(nums[i]);
        backtrack(i+1, nums, subset, res);
        subset.remove(subset.size()-1);

        while(i+1<nums.length && nums[i]==nums[i+1]) i++;
        backtrack(i+1, nums, subset,res);
    }
}
```
