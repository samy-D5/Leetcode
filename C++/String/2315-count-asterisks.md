# 2315. Count Asterisks

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-asterisks/
**Tags:** String

## Approach 1 — 2025-06-15 23:57 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.4 MB*

```cpp
class Solution {
public:
    int countAsterisks(string s) {
        bool further=false;
        int count=0;
        for(int i=0;i<s.length();i++){
            if(s[i]=='|' && further==false)
            further=true;
            else if(s[i]=='|' && further==true)
            further=false;
            else if(s[i]=='*' && further==false)
            count++;
        }
        return count;
    }// If you find it helpful,please upvote me.
};
```
