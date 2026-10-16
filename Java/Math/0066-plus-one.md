# 66. Plus One

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/plus-one/
**Tags:** Array, Math

## Approach 1 — 2026-05-12 21:50 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.6 MB*

```java
class Solution {
    public int[] plusOne(int[] dig) {
        for(int i=dig.length-1; i>=0; i--){
            if(dig[i]+1!=10){
                dig[i]+=1;
                return dig;
            }
            dig[i]=0;
        }
        int[]ans = new int[dig.length+1];
        ans[0]=1;
        return ans;
    }
}
```
