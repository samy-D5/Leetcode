# 1829. Maximum XOR for Each Query

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/maximum-xor-for-each-query/
**Tags:** Array, Bit Manipulation, Prefix Sum

## Approach 1 — 2024-12-01 00:08 (java)

*Runtime: 2 ms (faster than 100.0%) · Memory: 58.8 MB*

```java
class Solution {
    public int[] getMaximumXor(int[] nums, int maximumBit) {
        int n = nums.length;
        int xorr = nums[0];
        int maxXor = (1 << maximumBit) - 1;

        for (int i = 1; i < n; i++) {
            xorr ^= nums[i];
        }

        int[] ans = new int[n];
        for (int i = 0; i < n; i++) {
            ans[i] = xorr ^ maxXor;
            xorr ^= nums[n - 1 - i];
        }

        return ans;
    }
}
```
