# 1816. Truncate Sentence

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/truncate-sentence/
**Tags:** Array, String

## Approach 1 — 2024-03-30 11:40 (java)

*Runtime: 1 ms (faster than 80.7%) · Memory: 41.4 MB*

```java
class Solution {
    public String truncateSentence(String s, int k) {
        StringBuilder str=new StringBuilder();
        for(int i=0;i<s.length();i++){
            if(s.charAt(i)==' ') k--;
            if(k==0) break;
            str.append(s.charAt(i));
            
        }
        return str.toString();
    }
}
```
