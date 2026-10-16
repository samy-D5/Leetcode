# 3324. Find the Sequence of Strings Appeared on the Screen

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/find-the-sequence-of-strings-appeared-on-the-screen/
**Tags:** String, Simulation

## Approach 1 — 2025-06-16 00:08 (cpp)

*Runtime: 31 ms (faster than 36.3%) · Memory: 95.1 MB*

```cpp
class Solution {
public:
    vector<string> stringSequence(string& target) {
        const int n=target.size();
        vector<string> ans;
        string word="";
        for (int i=0; i<n; i++){
            char c;
            for(c='a'; c<=target[i]; c++){
                ans.push_back(word+c);
            }
            word+=(c-1);
        }
        return ans;
    }
};
```
