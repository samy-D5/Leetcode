# 2037. Minimum Number of Moves to Seat Everyone

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-number-of-moves-to-seat-everyone/
**Tags:** Array, Greedy, Sorting, Counting Sort

## Approach 1 — 2024-06-13 10:41 (java)

*Runtime: 2 ms (faster than 94.4%) · Memory: 43.9 MB*

```java
class Solution {
    public int minMovesToSeat(int[] seats, int[] students) {
        Arrays.sort(seats);
        Arrays.sort(students);
        int ans=0;
        for(int i=0;i<seats.length;i++){
            ans+=Math.abs(seats[i]-students[i]);
        }
        return ans;
    }
}
```
