# 39. Combination Sum

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/combination-sum/
**Tags:** Array, Backtracking

## Approach 1 — 2025-11-26 20:13 (java)

*Runtime: 2 ms (faster than 93.3%) · Memory: 45.8 MB*

```java
class Solution {
    public List<List<Integer>> combinationSum(int[] candidates, int target) {
        List<List<Integer>> res = new ArrayList<>();

        findCombinationSum(candidates, target, 0, new ArrayList<>(), 0, res);
        return res; 
    }

    private void findCombinationSum(int[] candidates, int target, int index, List<Integer> combination, int total, List<List<Integer>> ans){
        if(total==target){
            ans.add(new ArrayList<>(combination));
            return;
        }

        if(total > target || index >= candidates.length){
            return;
        }

        combination.add(candidates[index]);
        findCombinationSum(candidates, target, index, combination, total+candidates[index], ans);
        combination.remove(combination.size()-1);
        findCombinationSum(candidates, target, index+1, combination, total,ans);

    }
}
```

## Approach 2 — 2025-11-27 09:17 (java)

*Runtime: 2 ms (faster than 93.3%) · Memory: 45.7 MB*

```java
class Solution {
    public List<List<Integer>> combinationSum(int[] candidates, int target) {
        List<List<Integer>> ans = new ArrayList<>();
        backtrack(candidates, target, 0, new ArrayList<>(), ans);
        return ans;
    }

    private void backtrack(int[] arr, int remain, int idx, List<Integer> path, List<List<Integer>> ans) {
        if (remain == 0) {
            ans.add(new ArrayList<>(path));
            return;
        }
        if (idx == arr.length || remain < 0) return;

        path.add(arr[idx]);
        backtrack(arr, remain - arr[idx], idx, path, ans);
        path.remove(path.size() - 1);

        //skip current candidate and move to next
        backtrack(arr, remain, idx + 1, path, ans);
    }
}
```
