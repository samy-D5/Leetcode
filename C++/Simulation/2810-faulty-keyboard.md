# 2810. Faulty Keyboard

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/faulty-keyboard/
**Tags:** String, Simulation

## Approach 1 — 2025-06-16 00:13 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 9.5 MB*

```cpp
class Solution {
public:
    string finalString(string s) {
        string ans;
        for(char c : s)
        {
            if(c=='i') reverse(ans.begin(),ans.end());
            else ans+=c;
        }
        return ans;

    }
};
```
