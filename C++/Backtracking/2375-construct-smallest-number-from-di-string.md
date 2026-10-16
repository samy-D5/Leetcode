# 2375. Construct Smallest Number From DI String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/construct-smallest-number-from-di-string/
**Tags:** String, Backtracking, Stack, Greedy

## Approach 1 — 2025-06-15 23:55 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.1 MB*

```cpp
class Solution {
public:
    string smallestNumber(string pattern) {
        int n = pattern.length();
        string result = "";
        int stack[n + 1];
        int index = 0;

        for (int i = 0; i <= n; i++) {
            stack[index++] = i + 1;

            if (i == n || pattern[i] == 'I') {
                while (index > 0) {
                    result += to_string(stack[--index]);
                }
            }
        }

        return result;
    }
};
```
