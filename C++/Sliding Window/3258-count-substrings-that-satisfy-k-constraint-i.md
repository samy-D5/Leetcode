# 3258. Count Substrings That Satisfy K-Constraint I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-substrings-that-satisfy-k-constraint-i/
**Tags:** String, Sliding Window

## Approach 1 — 2025-06-16 00:17 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 9 MB*

```cpp
class Solution {
public:
    int countKConstraintSubstrings(string s, int k) {
        int l = 0, r = 0;
        int one = 0, zero = 0;
        int ans = 0;

        while (r < s.size()) {
            if (s[r] == '0') zero++;
            else one++;
            
            while (zero > k && one > k) { // Both exceed k, so we need to shrink the window
                if (s[l] == '0') zero--;
                else one--;
                l++;
            }

            ans += (r - l + 1); // All substrings ending at r and starting from l to r are valid
            r++;
        }

        return ans;
    }
};
```
