# 2337. Move Pieces to Obtain a String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/move-pieces-to-obtain-a-string/
**Tags:** Two Pointers, String

## Approach 1 — 2024-12-06 00:58 (java)

*Runtime: 105 ms (faster than 5.0%) · Memory: 45.7 MB*

```java
class Solution {
    public boolean canChange(String start, String target) {
        if (!(start.replaceAll("_", "")).equals(target.replaceAll("_", ""))) 
            return false;
        for (int i = 0, j = 0, n = start.length(); i < n && j < n; ++i, ++j) {
            while (i < n && start.charAt(i) == '_') ++i;
            while (j < n && target.charAt(j) == '_') ++j;
            if (i < n && j < n && (start.charAt(i) == 'L' && i < j || target.charAt(j) == 'R' && i > j))
                return false;
        }
        return true;
    }
}
```
