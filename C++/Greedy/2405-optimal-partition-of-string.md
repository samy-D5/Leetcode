# 2405. Optimal Partition of String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/optimal-partition-of-string/
**Tags:** Hash Table, String, Greedy

## Approach 1 — 2025-06-16 00:14 (cpp)

*Runtime: 3 ms (faster than 87.6%) · Memory: 13.1 MB*

```cpp
class Solution {
public:
    int partitionString(string s) {
        int i = 0, ans = 1,flag = 0;
        while(i < s.size()){
            int val = s[i] - 'a';
            if( flag & (1<<val) ) {
                flag = 0;
                ans++;
            }
            flag = flag | (1<<val);
            i++;
        }
        return ans;
    }
};
```
