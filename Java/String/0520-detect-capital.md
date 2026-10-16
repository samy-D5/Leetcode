# 520. Detect Capital

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/detect-capital/
**Tags:** String

## Approach 1 — 2024-07-31 00:03 (java)

*Runtime: 1 ms (faster than 89.1%) · Memory: 41.4 MB*

```java
class Solution {
    public boolean detectCapitalUse(String word) {
        int count=0;
        for(char x:word.toCharArray()){
            if(Character.isUpperCase(x)==true) count++;
        }
        if(count==word.length() || count==0) return true;
        else if(count==1 && Character.isUpperCase(word.charAt(0))) return true;
        return false;
    }
}
```
