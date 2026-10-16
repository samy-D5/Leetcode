# 2390. Removing Stars From a String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/removing-stars-from-a-string/
**Tags:** String, Stack, Simulation

## Approach 1 — 2025-06-16 00:15 (cpp)

*Runtime: 20 ms (faster than 49.1%) · Memory: 28.2 MB*

```cpp
class Solution {
public:
    string removeStars(string s) {
        string c="";
        for(int i=0;i<s.size();i++){
            if(s[i]=='*'){
                c.pop_back();
            }else{
                c+=s[i];
            }
            
        }
        return c;
    }
};
```
