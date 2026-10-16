# 14. Longest Common Prefix

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/longest-common-prefix/
**Tags:** Array, String, Trie

## Approach 1 — 2024-09-06 09:36 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41 MB*

```java
class Solution {
    public String longestCommonPrefix(String[] strs) {
        if (strs == null || strs.length == 0) return "";
        String prefix = strs[0];
       for (int i = 1; i < strs.length; i++) {
            while (strs[i].indexOf(prefix) != 0) {
                prefix = prefix.substring(0, prefix.length() - 1);
                if (prefix.isEmpty()) return "";
            }
        }
        return prefix;
    }
}
```
