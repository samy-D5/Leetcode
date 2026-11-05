# 202. Happy Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/happy-number/
**Tags:** Hash Table, Math, Two Pointers, Floyd's Cycle Finding Algorithm

## Approach 1 — 2026-11-05 18:11 (java)

*Runtime: 2 ms (faster than 22.6%) · Memory: 41.9 MB · Time to solve: 14m 57s (timer)*

```java
class Solution {
    public boolean isHappy(int n) {
        HashSet<Integer> set = new HashSet<>();

        while (n != 1 && !set.contains(n)) {
            set.add(n);
            n = happy(n);
        }

        return n == 1;
    }

    private int happy(int n) {
        int ans = 0;
        while (n > 0) {
            int digit = n % 10;
            ans = ans + (digit * digit);
            n = n / 10;
        }
        return ans;
    }
}
```
