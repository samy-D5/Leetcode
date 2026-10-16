# 1876. Substrings of Size Three with Distinct Characters

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/substrings-of-size-three-with-distinct-characters/
**Tags:** Hash Table, String, Sliding Window, Counting

## Approach 1 — 2025-11-14 00:35 (java)

*Runtime: 1 ms (faster than 95.8%) · Memory: 42.8 MB*

```java
class Solution {
    public int countGoodSubstrings(String s) {
        int count =0;
        for(int i=0 ; i<= s.length()-3 ; i++){
          char a = s.charAt(i);
          char b = s.charAt(i+1);
          char c = s.charAt(i+2);

          if(a!=b && b!=c && c!=a){
            count++;
          }
        }
        return count;
    }
}
```
