# 2678. Number of Senior Citizens

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-senior-citizens/
**Tags:** Array, String

## Approach 1 — 2025-06-16 00:04 (cpp)

*Runtime: 3 ms (faster than 8.9%) · Memory: 17.4 MB*

```cpp
class Solution {
public:
    int countSeniors(vector<string>& details) {
        int ans = 0;
        for (auto& x : details) {
            int age = stoi(x.substr(11, 2));
            ans += age > 60;
        }
        return ans;
    }
};
```
