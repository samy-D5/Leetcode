# 2744. Find Maximum Number of String Pairs

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-maximum-number-of-string-pairs/
**Tags:** Array, Hash Table, String, Simulation

## Approach 1 — 2025-06-15 23:58 (cpp)

*Runtime: 2 ms (faster than 65.1%) · Memory: 26.8 MB*

```cpp
class Solution {
public:
        int maximumNumberOfStringPairs(vector<string>& words) {
        int ans = 0;
        unordered_map<string, int> mp;
        for(auto w: words){
            string r = w;
            reverse(r.begin(), r.end());
            if(mp[r] > 0){ ans++; mp[r]--; }
            else mp[w]++;
        }
        return ans;
    }
};
```
