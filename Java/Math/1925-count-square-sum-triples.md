# 1925. Count Square Sum Triples

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-square-sum-triples/
**Tags:** Math, Enumeration

## Approach 1 — 2025-12-09 00:37 (java)

*Runtime: 12 ms (faster than 86.2%) · Memory: 42 MB*

```java
class Solution {
    public int countTriples(int n) {
        int count = 0;
        for (int a = 1; a <= n; a++) {
            for (int b = 1; b <= n; b++) {
                int c_sq = a * a + b * b;
                int c = (int) Math.sqrt(c_sq);
                if (c * c == c_sq && c <= n) {
                    count++;
                }
            }
        }
        return count;
    }
}
```
