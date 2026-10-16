# 1941. Check if All Characters Have Equal Number of Occurrences

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-all-characters-have-equal-number-of-occurrences/
**Tags:** Hash Table, String, Counting

## Approach 1 — 2025-06-16 00:13 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 9.2 MB*

```cpp
class Solution {
public:
    bool areOccurrencesEqual(string s){
        vector<int> cnt(26,0);
		//store freq of each char of s in cnt vector
        for(char c : s) cnt[c-'a']++;
		//num contains the freq of first char in s
        int num=cnt[s[0]-'a'];
		//traversing the cnt vector
		//freq in cnt must be either 0(char is not present in s) or num(if char present in s
		//than its freq should be same as that of other chars of string) else we will return false
        for(int i: cnt){
            if(i!=num and i!=0) return false;
        }
        return true;
    }
};
```
