# 2828. Check if a String Is an Acronym of Words

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-a-string-is-an-acronym-of-words/
**Tags:** Array, String

## Approach 1 — 2025-06-15 23:56 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.6 MB*

```cpp
class Solution {
public:
    bool isAcronym(vector<string>& words, string s) {
    string t = "";
    for(auto w: words) t += w[0];
    return t == s;
}
};
```
