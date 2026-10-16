# 1930. Unique Length-3 Palindromic Subsequences

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/unique-length-3-palindromic-subsequences/
**Tags:** Hash Table, String, Bit Manipulation, Prefix Sum

## Approach 1 — 2025-01-21 11:48 (java)

*Runtime: 295 ms (faster than 11.4%) · Memory: 45.5 MB*

```java
class Solution {
    public int countPalindromicSubsequence(String s) {
    int first[] = new int[26], last[] = new int[26], res = 0;
    Arrays.fill(first, Integer.MAX_VALUE);
    for (int i = 0; i < s.length(); ++i) {
        first[s.charAt(i) - 'a'] = Math.min(first[s.charAt(i) - 'a'], i);
        last[s.charAt(i) - 'a'] = i;
    }
    for (int i = 0; i < 26; ++i)
        if (first[i] < last[i])
            res += s.substring(first[i] + 1, last[i]).chars().distinct().count();
    return res;
}
}
```
