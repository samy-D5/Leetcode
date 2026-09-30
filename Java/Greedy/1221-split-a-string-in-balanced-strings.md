# 1221. Split a String in Balanced Strings

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/split-a-string-in-balanced-strings/
**Tags:** String, Greedy, Counting

## Approach 1 — 2026-09-30 11:24 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.7 MB*

```java
class Solution {
    public int balancedStringSplit(String s) {
        int sum=0,count=0;
        for(char c:s.toCharArray()){
            if(c=='R')  count++;
            else    count--;
            if(count==0)    sum+=1;
        }
        return sum;
    }
}
```
