# 2697. Lexicographically Smallest Palindrome

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/lexicographically-smallest-palindrome/
**Tags:** Two Pointers, String, Greedy

## Approach 1 — 2025-06-16 00:08 (cpp)

*Runtime: 3 ms (faster than 78.0%) · Memory: 18.3 MB*

```cpp
class Solution {
public:
        string makeSmallestPalindrome(string s) {
        int n = s.size();
        for (int i = 0; i < n; ++i)
            s[i] = s[n - 1 - i] = min(s[i], s[n - i - 1]);
        return s;
    }
};
```
