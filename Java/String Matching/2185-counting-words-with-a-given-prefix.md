# 2185. Counting Words With a Given Prefix

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/counting-words-with-a-given-prefix/
**Tags:** Array, String, String Matching

## Approach 1 — 2025-01-21 12:01 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.9 MB*

```java
class Solution {
    public int prefixCount(String[] words, String pref) {
        int c = 0, n = pref.length();
        for (String w : words) {
            if (w.length() >= n && w.startsWith(pref))
                c++;
        }
        return c;
    }
}
```
