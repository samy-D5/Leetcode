# 3162. Find the Number of Good Pairs I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-the-number-of-good-pairs-i/
**Tags:** Array, Hash Table

## Approach 1 — 2025-12-01 00:16 (java)

*Runtime: 1 ms (faster than 99.9%) · Memory: 44.6 MB*

```java
class Solution {
    public int numberOfPairs(int[] nums1, int[] nums2, int k) {
        int count = 0;
        for (int i : nums1) {
            for (int j : nums2) {
                if (i % (j * k) == 0) {
                    count++;
                }
            }
        }
        return count;
    }
}
```
