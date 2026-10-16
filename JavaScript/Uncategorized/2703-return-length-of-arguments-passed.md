# 2703. Return Length of Arguments Passed

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/return-length-of-arguments-passed/
**Tags:** 

## Approach 1 — 2024-08-11 23:14 (javascript)

*Runtime: 44 ms (faster than 48.9%) · Memory: 48.6 MB*

```javascript
/**
 * @param {...(null|boolean|number|string|Array|Object)} args
 * @return {number}
 */
var argumentsLength = function(...args) {
    return args.length;
};

/**
 * argumentsLength(1, 2, 3); // 3
 */
```

## Approach 2 — 2024-10-18 21:44 (javascript)

*Runtime: 64 ms (faster than 5.4%) · Memory: 48.9 MB*

```javascript
/**
 * @param {...(null|boolean|number|string|Array|Object)} args
 * @return {number}
 */
var argumentsLength = function(...args) {
    return args.length
};

/**
 * argumentsLength(1, 2, 3); // 3
 */
```
