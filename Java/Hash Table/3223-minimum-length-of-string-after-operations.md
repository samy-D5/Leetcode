# 3223. Minimum Length of String After Operations

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-length-of-string-after-operations/
**Tags:** Hash Table, String, Counting

## Approach 1 — 2025-01-21 12:05 (java)

*Runtime: 92 ms (faster than 8.3%) · Memory: 46.4 MB*

```java
class Solution {
    public int minimumLength(String s) {
        int n = s.length(), del = 0;
        Map<Character, Integer> mp = new HashMap<>();
        for (int i = 0; i < n; i++) {
            mp.put(s.charAt(i), mp.getOrDefault(s.charAt(i), 0) + 1);
        }
        for (Map.Entry<Character, Integer> entry : mp.entrySet()) {
            int f = entry.getValue();
            del += (f % 2 == 1) ? f - 1 : f - 2;
        }
        return n - del;
    }
}
```
