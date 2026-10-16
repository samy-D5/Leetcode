# 1769. Minimum Number of Operations to Move All Balls to Each Box

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-number-of-operations-to-move-all-balls-to-each-box/
**Tags:** Array, String, Prefix Sum

## Approach 1 — 2025-01-21 11:51 (java)

*Runtime: 3 ms (faster than 97.8%) · Memory: 44.7 MB*

```java
class Solution {
    public int[] minOperations(String boxes) {
        int n = boxes.length();
        int[] distances = new int[n];
        int prefixCount = 0, prefixSum = 0;
        for (int i = 0; i < n; ++i) {
            distances[i] = prefixCount * i - prefixSum;
            if (boxes.charAt(i) == '1') {
                ++prefixCount;
                prefixSum += i;
            }
        }
        int suffixCount=0, suffixSum = 0;
        for (int i = n - 1; i >= 0; --i) {
            distances[i] += suffixSum - suffixCount * i;
            if (boxes.charAt(i) == '1') {
                ++suffixCount;
                suffixSum += i;
            }
        }
        return distances;
    }
}
```
