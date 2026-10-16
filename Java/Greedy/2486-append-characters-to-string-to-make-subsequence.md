# 2486. Append Characters to String to Make Subsequence

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/append-characters-to-string-to-make-subsequence/
**Tags:** Two Pointers, String, Greedy

## Approach 1 — 2024-06-03 23:19 (java)

*Runtime: 4 ms (faster than 98.4%) · Memory: 45.3 MB*

```java
class Solution {
    public int appendCharacters(String s, String t) {
        int sIndex = 0, tIndex = 0;
        int sLength = s.length(), tLength = t.length();
        
        while (sIndex < sLength && tIndex < tLength) {
            if (s.charAt(sIndex) == t.charAt(tIndex)) {
                tIndex++;
            }
            sIndex++;
        }
        
        return tLength - tIndex;
        
    }
}
```
