# 3034. Number of Subarrays That Match a Pattern I

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/number-of-subarrays-that-match-a-pattern-i/
**Tags:** Array, Rolling Hash, String Matching, Hash Function

## Approach 1 — 2025-11-24 23:42 (java)

*Runtime: 2 ms (faster than 13.7%) · Memory: 46.1 MB*

```java
class Solution {
    public int countMatchingSubarrays(int[] nums, int[] pattern) {
        int m = pattern.length;
        int n = nums.length;
        int count = 0;
        for (int i = 0; i < n; i++) {
            for (int j = i; j < n; j++) {
                if (j - i + 1 == m + 1) {
                    int l = i;
                    int flag = 0;
                    for (int k = 0; k < m; k++, l++) {
                        if (pattern[k] == 1 && nums[l + 1] > nums[l]) {
                            continue;
                        } else if (pattern[k] == 0 && nums[l + 1] == nums[l]) {
                            continue;
                        } else if (pattern[k] == -1 && nums[l + 1] < nums[l]) {
                            continue;
                        } else {
                            flag = 1;
                            break;
                        }
                    }
                    if (flag == 0)  count++;
                }
            }
        }
        return count;
    }
}
```
