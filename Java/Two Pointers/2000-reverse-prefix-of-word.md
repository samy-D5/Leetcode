# 2000. Reverse Prefix of Word

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reverse-prefix-of-word/
**Tags:** Two Pointers, String, Stack

## Approach 1 — 2024-12-26 23:42 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.7 MB*

```java
class Solution {
    public String reversePrefix(String word, char ch) {
        int firstOccurence = word.indexOf(ch);
        if (firstOccurence == -1) {
            return word;
        }
        StringBuilder sb = new StringBuilder(word.substring(0, firstOccurence + 1)).reverse();
        if (firstOccurence < word.length()) {
            sb.append(word.substring(firstOccurence + 1));
        }
        return sb.toString();
    }
}
```
