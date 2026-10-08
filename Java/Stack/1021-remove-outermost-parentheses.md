# 1021. Remove Outermost Parentheses

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/remove-outermost-parentheses/
**Tags:** String, Stack, Bracket Sequences

## Approach 1 — 2026-10-09 00:15 (java)

*Runtime: 4 ms (faster than 58.5%) · Memory: 43.6 MB · Time to solve: 40m 12s*

```java
class Solution {
    public String removeOuterParentheses(String s) {
       StringBuilder str = new StringBuilder();
       int open=1;

       if(s.length()<=2) return ""; 

       for(int i=1; i<s.length(); i++){
        if(s.charAt(i)=='('){
            open++;
            if(open>1) str.append('(');
        }else{
            if(open>1) str.append(')');
            open--;
        }
       } 
        return str.toString();
    }
}
```
