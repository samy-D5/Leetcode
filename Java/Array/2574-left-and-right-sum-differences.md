# 2574. Left and Right Sum Differences

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/left-and-right-sum-differences/
**Tags:** Array, Prefix Sum

## Approach 1 — 2024-07-12 23:29 (java)

*Runtime: 2 ms (faster than 98.7%) · Memory: 44.6 MB*

```java
class Solution {
    public int[] leftRightDifference(int[] arr) {
        int n = arr.length;
        int l[] = new int[n];
        int r[] = new int[n];
        l[0] = 0;
        r[n-1] = 0;
        for(int i=1; i<n; i++){
            l[i] = l[i-1]+arr[i-1];
        }

        for(int i=n-2; i>=0; i--){
            r[i] = r[i+1]+arr[i+1];
        }

        int ans[] = new int[n];
        for(int i=0; i<n; i++){
            ans[i] = Math.abs(l[i]-r[i]);
        }
        return ans;
    }
}
```
