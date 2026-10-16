# 1689. Partitioning Into Minimum Number Of Deci-Binary Numbers

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/partitioning-into-minimum-number-of-deci-binary-numbers/
**Tags:** String, Greedy

## Approach 1 — 2025-06-15 23:54 (cpp)

*Runtime: 3 ms (faster than 39.7%) · Memory: 16.6 MB*

```cpp
class Solution {
public:
    int minPartitions(string n) {
        std::string::iterator itr=n.begin(),temp=n.begin();
        while(itr!=n.end())
        {
            if(*itr>*temp)
                temp=itr;
            itr++;
        }
        return *temp-48;
    }
};
```
