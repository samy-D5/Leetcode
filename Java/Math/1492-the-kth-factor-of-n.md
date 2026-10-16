# 1492. The kth Factor of n

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/the-kth-factor-of-n/
**Tags:** Math, Number Theory, Prime Factorization

## Approach 1 — 2024-06-01 13:49 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.3 MB*

```java
class Solution {
    public int kthFactor(int n, int k) {
        int count=0;
        for(int i=1;i<=n;i++){
            if(n%i==0) count++;
            if(count==k) return i;
        }
         return -1;
    }
}
```
