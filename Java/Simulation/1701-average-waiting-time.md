# 1701. Average Waiting Time

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/average-waiting-time/
**Tags:** Array, Simulation

## Approach 1 — 2024-07-10 00:07 (java)

*Runtime: 3 ms (faster than 96.9%) · Memory: 72.9 MB*

```java
class Solution {
    public double averageWaitingTime(int[][] customers) {
        double total_waiting_time = 0;
        int current_time = 0;

        for (int[] customer : customers) {
            int arrival = customer[0];
            int service = customer[1];
            if (current_time < arrival) {
                current_time = arrival;
            }
            int waiting_time = current_time - arrival + service;
            total_waiting_time += waiting_time;
            current_time += service;
        }

        return total_waiting_time / customers.length;
    }
}
```
