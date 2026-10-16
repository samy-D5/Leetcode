# 1768. Merge Strings Alternately

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/merge-strings-alternately/
**Tags:** Two Pointers, String

## Approach 1 — 2025-06-15 23:58 (cpp)

*Runtime: 4 ms (faster than 33.1%) · Memory: 8.3 MB*

```cpp
class Solution {
public:
    string mergeAlternately(string word1, string word2) {
        string result = "";
        int i = 0;
        while (i < word1.length() || i < word2.length()) {
            if (i < word1.length()) {
                result += word1[i];
            }
            if (i < word2.length()) {
                result += word2[i];
            }
            i++;
        }
        return result;
    }
};
```
