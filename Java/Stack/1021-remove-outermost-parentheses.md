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

**AI Analysis:**

- **Complexity:** Time: O(n) · Space: O(n)
- **Approach:** The algorithm tracks the nesting depth of parentheses using an integer counter (`open`) initialized to 1 for the first character. As it iterates through the remaining characters, it only appends an opening parenthesis if the depth is greater than 1 after incrementing, and only appends a closing parenthesis if the depth is greater than 1 before decrementing. This effectively filters out the outermost parentheses of each primitive decomposition without needing an explicit stack.
- **Pattern:** Balance Counter (Stack Simulation) - Tracks parentheses nesting depth with a counter instead of a full stack because the string is guaranteed to be valid and only one bracket type is present.

