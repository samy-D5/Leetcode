# 1678. Goal Parser Interpretation

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/goal-parser-interpretation/
**Tags:** String

## Approach 1 — 2025-06-09 12:27 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.7 MB*

```java
class Solution {
    public String interpret(String c) {
        StringBuilder s = new StringBuilder (c.length());

        for(int i=0; i<c.length(); i++){
            if(c.charAt(i) == 'G') s.append('G');
            if(c.charAt(i) == '('){
                if(c.charAt(i+1)== ')') {
                    s.append('o');
                    i++;
                } else {
                    s.append("al");
                    i += 3;
                }
            }
        }
        return s.toString();
}
}
```
