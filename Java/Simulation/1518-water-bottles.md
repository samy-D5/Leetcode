# 1518. Water Bottles

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/water-bottles/
**Tags:** Math, Simulation

## Approach 1 — 2024-07-07 23:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.1 MB*

```java
class Solution {
    public int numWaterBottles(int numBottles, int numExchange) {
        int totalBottles = numBottles;

        while (numBottles >= numExchange) {
            totalBottles += numBottles / numExchange;
            numBottles = (numBottles / numExchange) + (numBottles % numExchange);
        }

        return totalBottles;
    }
}
```
