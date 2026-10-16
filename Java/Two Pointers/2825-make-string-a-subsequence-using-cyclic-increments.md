# 2825. Make String a Subsequence Using Cyclic Increments

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/make-string-a-subsequence-using-cyclic-increments/
**Tags:** Two Pointers, String

## Approach 1 — 2024-12-04 23:46 (java)

*Runtime: 5 ms (faster than 97.9%) · Memory: 46.1 MB*

```java
class Solution {
    public static boolean canMakeSubsequence(String source, String target) {
        int srcLen = source.length(), tgtLen = target.length();
        char targetChar = target.charAt(0);
        
        int srcIdx = 0, tgtIdx = 0;
        while (srcIdx < srcLen && tgtIdx < tgtLen) {
            char srcChar = source.charAt(srcIdx);
            
            if (srcChar == targetChar || 
                (char)(srcChar + 1) == targetChar || 
                (srcChar == 'z' && targetChar == 'a')) {
                tgtIdx++;
                if (tgtIdx < tgtLen) {
                    targetChar = target.charAt(tgtIdx);
                }
            }
            
            srcIdx++;
        }
        
        return tgtIdx == tgtLen;
    }
}
```
