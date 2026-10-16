# 2710. Remove Trailing Zeros From a String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/remove-trailing-zeros-from-a-string/
**Tags:** String

## Approach 1 — 2025-06-16 00:12 (cpp)

*Runtime: 1 ms (faster than 44.6%) · Memory: 11.8 MB*

```cpp
class Solution {
public:
    string removeTrailingZeros(string num) {
    int i = num.size() -1; 
    while(i >= 0 && num[i] == '0') i--;
    return num.substr(0, i+1);
}
};
```
