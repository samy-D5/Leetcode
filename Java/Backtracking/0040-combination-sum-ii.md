# 40. Combination Sum II

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/combination-sum-ii/
**Tags:** Array, Backtracking

## Approach 1 — 2025-11-27 09:34 (java)

*Runtime: 5 ms (faster than 98.3%) · Memory: 44.7 MB*

```java
class Solution {
    public List<List<Integer>> combinationSum2(int[] candidates, int target) {
        List<List<Integer>> ans = new ArrayList<>();
        Arrays.sort(candidates);
        backtrack(candidates, target, 0, new ArrayList<>(), ans);
        return ans;
    }

    private void backtrack(int[] arr, int remain, int idx, List<Integer> path, List<List<Integer>> ans) {
        if (remain == 0) {
            ans.add(new ArrayList<>(path));
            return;
        }
        for (int i = idx; i < arr.length; i++) {
            if (i > idx && arr[i] == arr[i - 1]) continue;
            if (arr[i] > remain) break;

        path.add(arr[i]);
        backtrack(arr, remain - arr[i], i+1, path, ans);
        path.remove(path.size() - 1);
        }
        // backtrack(arr, remain, idx + 1, path, ans);
    }
}
```
