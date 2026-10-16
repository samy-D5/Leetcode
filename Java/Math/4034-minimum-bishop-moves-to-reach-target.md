# 4034. Minimum Bishop Moves to Reach Target

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-bishop-moves-to-reach-target/
**Tags:** Array, Math

## Approach 1 — 2026-09-01 23:13 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.2 MB*

```java
class Solution {
    public int minBishopMoves(int[] s, int[] tar) {
        if((s[0]+s[1])%2 != (tar[0]+tar[1])%2) return -1;
        else{
            if((s[0]==tar[0] && s[1]==tar[1])) return 0;
           else if((s[0]+s[1])==(tar[0]+tar[1]) || (s[0]-s[1])==(tar[0]-tar[1])) return 1;
           else return 2; 
        }
    }
}
```
