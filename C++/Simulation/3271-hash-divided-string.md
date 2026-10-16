# 3271. Hash Divided String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/hash-divided-string/
**Tags:** String, Simulation

## Approach 1 — 2025-06-15 23:57 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 11.3 MB*

```cpp
class Solution {
public:
    string stringHash(string s, int k) {
        string ans="";
        for(int i=0;i<s.size();i+=k)
        {
            int sum=0;
            for(int j=0;j<k;++j)
                sum+=s[i+j]-'a';
            sum=sum%26;
            ans+=(char)(sum+'a');
        }
        return ans;
    }
};
```
