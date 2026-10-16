# 2433. Find The Original Array of Prefix Xor

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/find-the-original-array-of-prefix-xor/
**Tags:** Array, Bit Manipulation

## Approach 1 — 2024-09-05 21:32 (java)

*Runtime: 2 ms (faster than 93.3%) · Memory: 56.7 MB*

```java
class Solution {
    public int[] findArray(int[] pref) {
        int ans[]=new int[pref.length];
        ans[0]=pref[0];
        for(int i=1;i<pref.length;i++){
            ans[i]=pref[i-1]^pref[i];
        }
        return ans;
    }
}
```
