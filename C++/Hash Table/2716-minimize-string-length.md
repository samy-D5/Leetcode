# 2716. Minimize String Length

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimize-string-length/
**Tags:** Hash Table, String

## Approach 1 — 2025-06-16 00:17 (cpp)

*Runtime: 26 ms (faster than 14.3%) · Memory: 16.8 MB*

```cpp
class Solution {
public:
    int minimizedStringLength(string s) {
        return unordered_set<char>(s.begin(), s.end()).size();
    }
};
```
