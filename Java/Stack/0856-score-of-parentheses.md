# 856. Score of Parentheses

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/score-of-parentheses/
**Tags:** String, Stack, Bracket Sequences

## Approach 1 — 2026-10-05 23:20 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.7 MB*

```java
class Solution {
    public int scoreOfParentheses(String S) {
        return A(S, 0, S.length());
    }
    private int A(String S, int i, int j){
        int ans=0, bal=0;

        for(int k=i; k<j; ++k){
            bal+= S.charAt(k)=='(' ? 1:-1;
            if(bal==0){
                if(k-i==1) ans++;
                else ans+= 2*A(S,i+1, k);
                i=k+1;
            }
        }
        return ans;
    }
}
```
