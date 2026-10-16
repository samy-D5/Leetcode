# 2723. Add Two Promises

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/add-two-promises/
**Tags:** 

## Approach 1 — 2024-10-18 21:50 (javascript)

*Runtime: 65 ms (faster than 7.8%) · Memory: 49.7 MB*

```javascript
/**
 * @param {Promise} promise1
 * @param {Promise} promise2
 * @return {Promise}
 */
var addTwoPromises = async function(promise1, promise2) {
    const [val1, val2] = await Promise.all([promise1, promise2]);
    return val1+val2;
};

/**
 * addTwoPromises(Promise.resolve(2), Promise.resolve(2))
 *   .then(console.log); // 4
 */
```
