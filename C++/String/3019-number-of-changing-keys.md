# 3019. Number of Changing Keys

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-changing-keys/
**Tags:** String

## Approach 1 — 2025-06-16 00:10 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 9.1 MB*

```cpp
class Solution {
public:
    int countKeyChanges(string s) {
    int count = 0;
    for (int i = 1; i < s.size(); i++) {
        if (toupper(s[i]) != toupper(s[i - 1])) {
            count++;
        }
    }
    return count;
}

};
```
