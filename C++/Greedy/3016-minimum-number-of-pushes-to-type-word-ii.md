# 3016. Minimum Number of Pushes to Type Word II

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimum-number-of-pushes-to-type-word-ii/
**Tags:** Hash Table, String, Greedy, Sorting, Counting

## Approach 1 — 2025-06-16 00:10 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 28.5 MB*

```cpp
class Solution {
public:
    int minimumPushes(string word) {
        vector<int> letterFreq(26, 0);
        for (char c : word) {
            letterFreq[c - 'a']++;
        }
        
        sort(letterFreq.rbegin(), letterFreq.rend());
        
        int totalPresses = 0;
        for (int i = 0; i < 26; i++) {
            if (letterFreq[i] == 0) break;
            totalPresses += (i / 8 + 1) * letterFreq[i];
        }
        
        return totalPresses;
    }
};
```
