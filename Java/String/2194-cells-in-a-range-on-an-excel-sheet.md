# 2194. Cells in a Range on an Excel Sheet

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/cells-in-a-range-on-an-excel-sheet/
**Tags:** String

## Approach 1 — 2024-03-30 14:01 (java)

*Runtime: 5 ms (faster than 23.0%) · Memory: 45 MB*

```java
class Solution {
    public List<String> cellsInRange(String s) {
       char startCol=  s.charAt(0);
       char startRow=  s.charAt(1);
       char endCol=  s.charAt(3);
       char endRow=  s.charAt(4);
       char temp=startRow;

       List<String> ans=new ArrayList<>();

       while(startCol<=endCol){
        while(startRow<=endRow){
            ans.add(""+startCol+startRow);
            startRow++;
        }
            startCol++;
            startRow=temp;
       }
       return ans;
    }
}
```
