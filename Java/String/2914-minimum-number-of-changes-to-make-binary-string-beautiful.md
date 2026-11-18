# 2914. Minimum Number of Changes to Make Binary String Beautiful

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-number-of-changes-to-make-binary-string-beautiful/
**Tags:** String

## Approach 1 — 2026-11-18 12:32 (java)

*Runtime: 3 ms (faster than 97.6%) · Memory: 46.2 MB · Time to solve: 19m 30s (timer)*

```java
class Solution {
    public int minChanges(String s) {
        int count=0;
        for(int i=0; i<s.length(); i+=2){
            if(s.charAt(i)!=s.charAt(i+1)) count++;
        }
        return count;
    }
}
```
