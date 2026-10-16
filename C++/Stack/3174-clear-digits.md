# 3174. Clear Digits

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/clear-digits/
**Tags:** String, Stack, Simulation

## Approach 1 — 2025-06-15 23:56 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.3 MB*

```cpp
class Solution {
public:
    static string clearDigits(string& s) {
        int n=s.size(), j=0;
        for(int i=0; i<n; i++){
            if (isdigit(s[i]) && j>0) j--;
            else  s[j++]=s[i]; 
        }
        s.resize(j);
        return s;
    }
};
```
