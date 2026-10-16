# 3498. Reverse Degree of a String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reverse-degree-of-a-string/
**Tags:** String, Simulation

## Approach 1 — 2025-06-15 23:54 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 9.5 MB*

```cpp
class Solution {
public:
    int reverseDegree(const std::string& s) {
        int ans = 0, idx = 1;
        for (char ch : s) {
            ans += (123 - static_cast<int>(ch)) * idx;
            idx++;}
        return ans;}
};
```
