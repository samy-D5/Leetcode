# 3345. Smallest Divisible Digit Product I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/smallest-divisible-digit-product-i/
**Tags:** Math, Enumeration

## Approach 1 — 2026-08-07 01:42 (python)

*Runtime: 0 ms (faster than 100.0%) · Memory: 19.3 MB*

```python
class Solution:
    def smallestNumber(self, n: int, t: int) -> int:
        q, r = divmod(n, 10)
        req = t // gcd(max(q, 1), t)
        nxt = ((r + req - 1) // req) * req
        x = nxt - (nxt - 10) * (nxt // 10)

        return q * 10 + x
```
