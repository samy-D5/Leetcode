# 2490. Circular Sentence

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/circular-sentence/
**Tags:** String

## Approach 1 — 2024-11-20 22:56 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.6 MB*

```java
class Solution {
    public boolean isCircularSentence(String str) {
        if(str.charAt(0)!=str.charAt(str.length()-1)) return false;
        int space = str.indexOf(" ");
        if(space==-1) return true;
        while(space>-1){
              if(str.charAt(space-1)!= str.charAt(space+1)) return false;
              space = str.indexOf(" ",space+1);
        }
        return true;
    }
}
```
