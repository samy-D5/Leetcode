# 2667. Create Hello World Function

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/create-hello-world-function/
**Tags:** 

## Approach 1 — 2025-12-04 01:03 (javascript)

*Runtime: 41 ms (faster than 61.7%) · Memory: 53.9 MB*

```javascript
/**
 * @return {Function}
 */
var createHelloWorld = function() {
    const greeting ="Hello World";
    return function(...args) {
        return greeting;
    }
};

/**
 * const f = createHelloWorld();
 * f(); // "Hello World"
 */
```
