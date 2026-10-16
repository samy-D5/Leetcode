# 3222. Find the Winning Player in Coin Game

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-the-winning-player-in-coin-game/
**Tags:** Math, Simulation, Game Theory

## Approach 1 — 2024-07-20 21:04 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.4 MB*

```java
class Solution {
    public String losingPlayer(int x, int y) {
       while(true){
        //Alice 
        if(x<1 || y<4) return "Bob";
        x--;
        y-=4;
        //Bob
        if(x<1 || y<4) return "Alice";
        x--;
        y-=4;
       }
    }
}
```
