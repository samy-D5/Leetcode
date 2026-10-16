# 2381. Shifting Letters II

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/shifting-letters-ii/
**Tags:** Array, String, Prefix Sum

## Approach 1 — 2025-01-21 11:50 (java)

*Runtime: 7 ms (faster than 78.5%) · Memory: 76.3 MB*

```java
class Solution {
    public String shiftingLetters(String s, int[][] shifts) {
        int n = s.length();
        int[] shift = new int[n + 1];
        for (int[] shiftOp : shifts) {
            int start = shiftOp[0], end = shiftOp[1], direction = shiftOp[2];
            shift[start] += (direction == 1 ? 1 : -1);
            if (end + 1 < n) shift[end + 1] -= (direction == 1 ? 1 : -1);
        }
        int currentShift = 0;
        for (int i = 0; i < n; ++i) {
            currentShift += shift[i];
            shift[i] = currentShift;
        }
        StringBuilder result = new StringBuilder(s);
        for (int i = 0; i < n; ++i) {
            int netShift = (shift[i] % 26 + 26) % 26;
            result.setCharAt(i, (char) ('a' + (s.charAt(i) - 'a' + netShift) % 26));
        }
        return result.toString();
    }
}
```
