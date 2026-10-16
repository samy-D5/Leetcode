# 3379. Transformed Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/transformed-array/
**Tags:** Array, Simulation

## Approach 1 — 2026-05-14 09:11 (python)

*Runtime: 70 ms (faster than 11.6%) · Memory: 19.2 MB*

```python
class Solution:
    def constructTransformedArray(self, nums: List[int]) -> List[int]:
        return [nums[(i+x)%len(nums)] for i,x in enumerate(nums)]
```
