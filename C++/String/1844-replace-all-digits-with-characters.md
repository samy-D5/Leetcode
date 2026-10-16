# 1844. Replace All Digits with Characters

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/replace-all-digits-with-characters/
**Tags:** String

## Approach 1 — 2025-06-15 23:58 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.4 MB*

```cpp
class Solution {
public:
    string replaceDigits(string s) {
    for (auto i = 1; i < s.size(); i += 2)
        s[i] += s[i - 1] - '0';
    return s;
}
};
```
