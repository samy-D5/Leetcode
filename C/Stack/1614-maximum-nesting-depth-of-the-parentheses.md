# 1614. Maximum Nesting Depth of the Parentheses

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-nesting-depth-of-the-parentheses/
**Tags:** String, Stack, Bracket Sequences

## Approach 1 — 2025-06-08 16:02 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 7.9 MB*

```c
int maxDepth(char* s) {
    int count=0, res=0;

    for(int i=0; s[i]!='\0'; i++){
        if(s[i] == '('){
            count++;
            res = (count > res) ? count : res;
        } else if(s[i] == ')') count--;
    }
    return res;
}
```
