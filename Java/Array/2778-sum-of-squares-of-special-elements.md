# 2778. Sum of Squares of Special Elements 

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sum-of-squares-of-special-elements/
**Tags:** Array, Enumeration

## Approach 1 — 2026-10-14 00:04 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 46.3 MB · Time to solve: 14m 54s (timer)*

```java
class Solution {
    public int sumOfSquares(int[] nums) {
        int n=nums.length;
        int ans=0;
        for(int i=1; i<=n; i++){
            if(n%i==0) ans+= nums[i-1]*nums[i-1];
        }
        return ans;
    }
}
```
