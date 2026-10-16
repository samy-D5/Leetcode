# 3809. Best Reachable Tower

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/best-reachable-tower/
**Tags:** Array

## Approach 1 — 2026-01-17 21:10 (java)

*Runtime: 3 ms (faster than 70.1%) · Memory: 219.3 MB*

```java
class Solution {
    public int[] bestTower(int[][] towers, int[] center, int radius) {
        int maxq =0;
        int ptr =-1;
        int[] ans = new int[2];
        for(int i=0; i<towers.length; i++){
            if(Math.abs(towers[i][0]-center[0])
               +Math.abs(towers[i][1]-center[1])<=radius)
            {
                    if(towers[i][2] >maxq || ptr == -1){
                        maxq = towers[i][2];
                        ptr = i;
                    }else if(towers[i][2]==maxq){
                        if(towers[i][0]<towers[ptr][0] || (towers[i][0]==towers[ptr][0] && towers[i][1]<towers[ptr][1])){
                            ptr=i;
                        }
                    }
            }
        }
    
        if(ptr != -1){
            ans[0] = towers[ptr][0];
            ans[1] = towers[ptr][1];
            return ans;
        }else{
            ans[0] = -1;
            ans[1] = -1;
            return ans;
        }
    }
}
```
