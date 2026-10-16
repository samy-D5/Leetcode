# 1614. Maximum Nesting Depth of the Parentheses

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/
**Tags:** String, Stack, Bracket Sequences

## Approach 1 — 2025-06-08 15:59 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.5 MB*

```java
class Solution {
    public int maxDepth(String s) {
        int count=0, res=0;

        for(char c: s.toCharArray()){
            if(c == '('){
                count++;
                if(res < count) res= count;
            } else if(c == ')') count--;
        }
        return res;
    }
}
```
