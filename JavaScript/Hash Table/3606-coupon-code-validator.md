# 3606. Coupon Code Validator

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/coupon-code-validator/
**Tags:** Array, Hash Table, String, Sorting

## Approach 1 — 2025-12-14 00:34 (javascript)

*Runtime: 4 ms (faster than 72.7%) · Memory: 58.4 MB*

```javascript
/**
 * @param {string[]} code
 * @param {string[]} businessLine
 * @param {boolean[]} isActive
 * @return {string[]}
 */
const categories = new Set(['electronics', 'grocery', 'pharmacy', 'restaurant']);
const regex = /^\w+$/;

const validateCoupons = (code, businessLine, isActive) => {
    const n = code.length;
    const valid = [];
    for (let i = 0; i < n; ++i) {
        if (isActive[i] && categories.has(businessLine[i]) && regex.test(code[i])) {
            valid.push(i);
        }
    }
    valid.sort((a, b) => {
        const dcat = businessLine[a].charCodeAt(0) - businessLine[b].charCodeAt(0);
        if (dcat !== 0) return dcat;
        const codea = code[a];
        const codeb = code[b];
        if (codea > codeb) return 1;
        if (codea < codeb) return -1;
        return 0;
    });
    const validCodes = [];
    const m = valid.length;
    for (let i = 0; i < m; ++i) {
        validCodes.push(code[valid[i]]);
    }
    return validCodes;
};
```
