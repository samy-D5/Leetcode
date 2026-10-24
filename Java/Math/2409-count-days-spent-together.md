# 2409. Count Days Spent Together

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-days-spent-together/
**Tags:** Math, String

## Approach 1 — 2026-10-24 23:58 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.5 MB · Time to solve: 14m 54s (timer)*

```java
class Solution {
    public int countDaysTogether(String arriveAlice, String leaveAlice, String arriveBob, String leaveBob) {
        int[] days = {31, 28, 31, 30, 31, 30, 31, 31, 30, 31, 30, 31};
        int aStart = toDay(arriveAlice, days);
        int aEnd = toDay(leaveAlice, days);
        int bStart = toDay(arriveBob, days);
        int bEnd = toDay(leaveBob, days);
        int start = Math.max(aStart, bStart);
        int end = Math.min(aEnd, bEnd);
        return start <= end ? end - start + 1 : 0;
    }
    private int toDay(String s, int[] days) {
        int m = (s.charAt(0) - '0') * 10 + (s.charAt(1) - '0');
        int d = (s.charAt(3) - '0') * 10 + (s.charAt(4) - '0');
        int res = d;
        for (int i = 0; i < m - 1; i++) res += days[i];
        return res;
    }
}
```
