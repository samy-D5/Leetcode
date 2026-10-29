# 1. Two Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/two-sum/
**Tags:** Array, Hash Table

## Approach 1 — 2026-10-29 21:39 (python)

*Runtime: 1915 ms (faster than 7.6%) · Memory: 19.3 MB · Time to solve: 14m 54s (timer)*

```python
class Solution:
    def twoSum(self, nums: List[int], target: int) -> List[int]:
        Listt = []
        for i in range(0,len(nums)):
            for j in range(i+1, len(nums)):
                if(nums[i]+nums[j]==target):
                    Listt.extend([i,j])
        return Listt
```
