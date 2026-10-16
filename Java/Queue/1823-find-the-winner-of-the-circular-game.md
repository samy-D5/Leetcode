# 1823. Find the Winner of the Circular Game

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/find-the-winner-of-the-circular-game/
**Tags:** Array, Math, Recursion, Queue, Simulation

## Approach 1 — 2024-07-18 00:06 (java)

*Runtime: 3 ms (faster than 61.4%) · Memory: 40.9 MB*

```java
class Solution {
    public int findTheWinner(int n, int k) {
        ArrayList<Integer> circle = new ArrayList<>();
        for (int i = 1; i <= n; ++i) {
            circle.add(i);
        }
        int cur_ind = 0;

        while (circle.size() > 1) {
            int next_to_remove = (cur_ind + k - 1) % circle.size();
            circle.remove(next_to_remove);
            cur_ind = next_to_remove;
        }

        return circle.get(0);
    }
}
```
