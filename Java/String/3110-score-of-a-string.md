# 3110. Score of a String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/score-of-a-string/
**Tags:** String

## Approach 1 — 2024-08-10 22:34 (java)

*Runtime: 1 ms (faster than 97.4%) · Memory: 42.1 MB*

```java
class Solution {
    public int scoreOfString(String s) {
        int sum=0;
        for(int i=0;i<s.length()-1;i++){
            sum+=Math.abs(s.charAt(i)-s.charAt(i+1));
        }
        return sum;
    }
}
```
