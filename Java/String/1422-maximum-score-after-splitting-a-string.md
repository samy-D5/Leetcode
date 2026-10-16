# 1422. Maximum Score After Splitting a String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-score-after-splitting-a-string/
**Tags:** String, Prefix Sum

## Approach 1 — 2025-01-21 11:44 (java)

*Runtime: 3 ms (faster than 25.6%) · Memory: 41.4 MB*

```java
public class Solution {
    public int maxScore(String s) {
        int maxScore = 0;
        int countZerosLeft = 0;
        int countOnesRight = (int) s.chars().filter(ch -> ch == '1').count();
        for (int i = 0; i < s.length() - 1; i++) {
            countZerosLeft += s.charAt(i) == '0' ? 1 : 0;
            countOnesRight -= s.charAt(i) == '1' ? 1 : 0;
            maxScore = Math.max(maxScore, countZerosLeft + countOnesRight);
        }
        return maxScore;
    }
}
```
