# 1967. Number of Strings That Appear as Substrings in Word

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-strings-that-appear-as-substrings-in-word/
**Tags:** Array, String

## Approach 1 — 2025-06-16 00:04 (cpp)

*Runtime: 3 ms (faster than 21.3%) · Memory: 11.7 MB*

```cpp
class Solution {
public:
    int numOfStrings(vector<string>& patterns, string word) {
        int counter = 0;
        
        for(auto p: patterns)
            if(word.find(p) != std::string::npos)
                ++counter;
        
        return counter;
    }
};
```
