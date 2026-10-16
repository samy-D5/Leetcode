# 3274. Check if Two Chessboard Squares Have the Same Color

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-two-chessboard-squares-have-the-same-color/
**Tags:** Math, String

## Approach 1 — 2024-12-23 05:26 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean checkTwoChessboards(String c1, String c2) {
        int s1=(c1.charAt(0)-'0')+(c1.charAt(1)-'0');
        int s2=(c2.charAt(0)-'0')+(c2.charAt(1)-'0');
        return s1%2==s2%2;
    }
}
```
