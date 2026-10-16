# 1980. Find Unique Binary String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/find-unique-binary-string/
**Tags:** Array, Hash Table, String, Backtracking

## Approach 1 — 2025-06-16 00:09 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 12.7 MB*

```cpp
class Solution {
public:
    string findDifferentBinaryString(vector<string>& nums) {
        string ans="";
        for(int i=0; i<nums.size(); i++) 
            ans+= nums[i][i]=='0' ? '1' : '0';          // Using ternary operator
			// ans+=to_string(1-(nums[i][i]-'0'));     // Alternate:  or use to_string & 1-x to flip
        return ans;
    }
};
```
