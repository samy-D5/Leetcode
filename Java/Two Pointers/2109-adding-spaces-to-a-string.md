# 2109. Adding Spaces to a String

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/adding-spaces-to-a-string/
**Tags:** Array, Two Pointers, String, Simulation

## Approach 1 — 2024-12-03 23:54 (java)

*Runtime: 25 ms (faster than 18.9%) · Memory: 82 MB*

```java
class Solution {
    public String addSpaces(String s, int[] spaces) {
        StringBuilder sb=new StringBuilder();

        sb.append(s.substring(0,spaces[0]));
        int i=1;
        for(; i<spaces.length; i++){
            sb.append(" ");
            sb.append(s.substring(spaces[i-1],spaces[i]));            
        }
        sb.append(" ");
        sb.append(s.substring(spaces[i-1])); 

        return sb.toString();
    }
}
```
