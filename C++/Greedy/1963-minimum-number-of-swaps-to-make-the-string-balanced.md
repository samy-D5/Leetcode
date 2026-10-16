# 1963. Minimum Number of Swaps to Make the String Balanced

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-number-of-swaps-to-make-the-string-balanced/
**Tags:** Two Pointers, String, Stack, Greedy, Bracket Sequences

## Approach 1 — 2025-06-16 00:14 (cpp)

*Runtime: 7 ms (faster than 88.6%) · Memory: 34.3 MB*

```cpp
class Solution {
public:
    int minSwaps(string s) {
        int size = 0;
        int n = s.size();
        for (int i = 0; i < n; i++) {
            char ch = s[i];
            if (ch == '[')
                size++;
            else if (size > 0) 
                size--;
        }
        return (size + 1) / 2;
    }
};
```
