# 2149. Rearrange Array Elements by Sign

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/rearrange-array-elements-by-sign/
**Tags:** Array, Two Pointers, Simulation

## Approach 1 — 2025-11-16 23:15 (java)

*Runtime: 5 ms (faster than 22.1%) · Memory: 176.7 MB*

```java
class Solution {
    public int[] rearrangeArray(int[] nums) {
        int n = nums.length;
        int[] pos = new int[n/2];
        int[] neg = new int[n/2];
        int p = 0, q = 0;
        for(int x : nums){
            if(x > 0) pos[p++] = x;
            else neg[q++] = x;
        }
        int[] ans = new int[n];
        int i = 0, j = 0, k = 0;
        while(i < n){
            ans[i++] = pos[j++];
            ans[i++] = neg[k++];
        }
        return ans;
    }
}
```
