# 2406. Divide Intervals Into Minimum Number of Groups

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/divide-intervals-into-minimum-number-of-groups/
**Tags:** Array, Two Pointers, Greedy, Sorting, Heap (Priority Queue), Prefix Sum

## Approach 1 — 2024-10-12 22:32 (java)

*Runtime: 33 ms (faster than 97.2%) · Memory: 80.4 MB*

```java
class Solution {
    public int minGroups(int[][] intervals) {
        int n = intervals.length;
        int[] start_times = new int[n];
        int[] end_times = new int[n];

        // Extract start and end times
        for (int i = 0; i < n; i++) {
            start_times[i] = intervals[i][0];
            end_times[i] = intervals[i][1];
        }

        // Sort start and end times
        Arrays.sort(start_times);
        Arrays.sort(end_times);

        int end_ptr = 0, group_count = 0;

        // Traverse through the start times
        for (int start : start_times) {
            if (start > end_times[end_ptr]) {
                end_ptr++;
            } else {
                group_count++;
            }
        }

        return group_count;
    }
}
```
