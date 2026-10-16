# 2957. Remove Adjacent Almost-Equal Characters

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/remove-adjacent-almost-equal-characters/
**Tags:** String, Dynamic Programming, Greedy

## Approach 1 — 2024-10-31 19:35 (java)

*Runtime: 1 ms (faster than 99.2%) · Memory: 41.8 MB*

```java
class Solution {
    public int removeAlmostEqualCharacters(String word) {
        int count=0;
        for(int i=0;i<word.length()-1;){
            char one=word.charAt(i);
            char two=word.charAt(i+1);
            if(one==two || (one+1)==two || (one-1)==two){
                count++;
                i+=2;
            }else i++;
        }
        return count;
    }
}
```
