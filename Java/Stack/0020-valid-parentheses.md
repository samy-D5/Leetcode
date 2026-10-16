# 20. Valid Parentheses

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/valid-parentheses/
**Tags:** String, Stack, Bracket Sequences

## Approach 1 — 2024-08-24 16:42 (java)

*Runtime: 1 ms (faster than 99.9%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean isValid(String s) {
        Stack<Character> stk = new Stack<>();
        for(char x:s.toCharArray()){
            if(x=='(' || x=='[' || x=='{') stk.push(x);
            else{
                if(stk.isEmpty()) return false;
                if((stk.peek()=='(' && x==')') ||
                    (stk.peek()=='[' && x==']') ||
                    (stk.peek()=='{' && x=='}')) stk.pop();
                else return false;
            }
           
        } return stk.size()==0;
    }
}
```
