# 2427. Number of Common Factors

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-common-factors/
**Tags:** Math, Enumeration, Number Theory, Euclidean Algorithm, Greatest Common Divisor

## Approach 1 — 2024-06-02 11:57 (java)

*Runtime: 1 ms (faster than 70.0%) · Memory: 40.6 MB*

```java
class Solution {
    public int commonFactors(int a, int b) {
        int count=0;
        int max=Math.max(a,b);

        for(int i=1;i<=max;i++){
            if(a%i==0 && b%i==0) count++;
        }
        return count;
    }
}
```
