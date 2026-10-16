# 2914. Minimum Number of Changes to Make Binary String Beautiful

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-number-of-changes-to-make-binary-string-beautiful/
**Tags:** String

## Approach 1 — 2025-06-16 00:19 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 12.8 MB*

```cpp
class Solution {
public:
    int minChanges(const std::string& s) {
    int count = 0;
    for (int i = 0; i < s.size() - 1; i += 2) {
        if (s[i] != s[i + 1]) {
            count++;
        }
    }
    return count;
}
};
#include <string>
```
