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

## Approach 2 — 2026-10-09 01:03 (java)

*Runtime: 8 ms (faster than 22.1%) · Memory: 42.8 MB · Time to solve: 12s (timer)*

```java
class Solution {
    public String removeOuterParentheses(String s) {
        Stack<Character> stacked = new Stack<>();
        StringBuilder str = new StringBuilder();

        for(int i=0; i<s.length(); i++){
            if(s.charAt(i)=='('){
                if(stacked.size()>0) str.append('(');
                stacked.push(s.charAt(i));
            }else{
                stacked.pop();
                if(stacked.size()>0) str.append(')');
            }
        }
        return str.toString();
    }
}
```

**AI Analysis:**

- **Complexity:** Time: O(n) · Space: O(n)
- **Approach:** Iterate through the input string while maintaining a stack to track the nesting depth of parentheses. When an opening bracket '(' is encountered, append it to the result only if the stack already contains elements (omitting the outermost bracket), then push it onto the stack. When a closing bracket ')' is encountered, pop from the stack first and append the bracket only if the stack remains non-empty.
- **Pattern:** Stack / Bracket Depth Tracking: Parentheses nesting levels can be modeled using a stack, where outermost brackets correspond strictly to transitions to and from a depth of zero.

