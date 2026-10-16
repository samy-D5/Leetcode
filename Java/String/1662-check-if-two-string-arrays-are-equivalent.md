# 1662. Check If Two String Arrays are Equivalent

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-two-string-arrays-are-equivalent/
**Tags:** Array, String

## Approach 1 — 2024-09-01 22:31 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.2 MB*

```java
class Solution {
    public boolean arrayStringsAreEqual(String[] w1, String[] w2) {
        StringBuilder a = new StringBuilder();
        StringBuilder b = new StringBuilder();
        for(String str:w1){
            a.append(str);
        }
        for(String str:w2){
            b.append(str);
        }
        return a.toString().equals(b.toString());
    }
}
```
