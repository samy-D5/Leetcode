# 2582. Pass the Pillow

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/pass-the-pillow/
**Tags:** Math, Simulation

## Approach 1 — 2024-07-06 17:22 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40 MB*

```java
class Solution {
    public int passThePillow(int n, int time) {
        boolean direc=true;
        int curr=1;
       for(int i=0;i<time;i++){
        if(direc){
            curr++;
            if(curr==n) direc=false;
        }
        else{
            curr--;
            if(curr==1) direc=true;
        }
     }
       return curr;
    }
}
```
