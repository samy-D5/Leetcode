# 2695. Array Wrapper

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/array-wrapper/
**Tags:** 

## Approach 1 — 2024-08-20 00:16 (javascript)

*Runtime: 65 ms (faster than 5.7%) · Memory: 50.7 MB*

```javascript
/**
 * @param {number[]} nums
 */
var ArrayWrapper = function(nums) {
        this.nums = nums;
};

ArrayWrapper.prototype.valueOf = function() {
    return this.nums.reduce((sum, num) => sum + num, 0);
}

ArrayWrapper.prototype.toString = function() {
    return `[${this.nums.join(',')}]`;
}
```
