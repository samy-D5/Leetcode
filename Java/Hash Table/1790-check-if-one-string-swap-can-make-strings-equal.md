# 1790. Check if One String Swap Can Make Strings Equal

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-one-string-swap-can-make-strings-equal/
**Tags:** Hash Table, String, Counting

## Approach 1 — 2025-02-21 23:11 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean areAlmostEqual(String s1, String s2) {
        int left = -1;
        int right = -1;
        int cnt = 0;

        for (int k = 0; k < s1.length(); k++) {
            if (s1.charAt(k) != s2.charAt(k)) {
                cnt++;
                if (left == -1)
                    left = k;
                else if (right == -1)
                    right = k;
            }
        }

        if (cnt == 0)
            return true;
        else if (cnt == 2 && s1.charAt(left) == s2.charAt(right) && s1.charAt(right) == s2.charAt(left)) 
            return true;

        return false;
    }
}
```
