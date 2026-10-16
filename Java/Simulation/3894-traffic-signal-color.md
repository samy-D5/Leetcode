# 3894. Traffic Signal Color

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/traffic-signal-color/
**Tags:** Math, String, Simulation

## Approach 1 — 2026-04-11 20:04 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.4 MB*

```java
class Solution {
    public String trafficSignal(int timer) {
        if(timer == 0){
            return "Green";
        }else if(timer == 30){
            return "Orange";
        }else if(timer <= 90 && timer > 30){
            return "Red";
        }
        return "Invalid";
    }
}
```
