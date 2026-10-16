# 1957. Delete Characters to Make Fancy String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/delete-characters-to-make-fancy-string/
**Tags:** String

## Approach 1 — 2024-11-11 00:29 (java)

*Runtime: 35 ms (faster than 67.8%) · Memory: 45.8 MB*

```java
class Solution {
    public String makeFancyString(String s) {
       StringBuilder sb = new StringBuilder();
       int count=1;
       for(int i=0;i<s.length();i++){
        if(i>0 && s.charAt(i) == s.charAt(i-1)) count++;
        else count =1;
        if(count <3) sb.append(s.charAt(i));
       }
       return sb.toString();
    }
}
```
