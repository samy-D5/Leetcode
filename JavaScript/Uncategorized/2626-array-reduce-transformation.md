# 2626. Array Reduce Transformation

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/array-reduce-transformation/
**Tags:** 

## Approach 1 — 2024-09-08 02:07 (javascript)

*Runtime: 60 ms (faster than 5.8%) · Memory: 49.1 MB*

```javascript
/**
 * @param {number[]} nums
 * @param {Function} fn
 * @param {number} init
 * @return {number}
 */
var reduce = function(nums, fn, init) {
    let val=init;
    for(let i=0;i<nums.length;i++)
        val=fn(val,nums[i]);
    return val;
};
```
