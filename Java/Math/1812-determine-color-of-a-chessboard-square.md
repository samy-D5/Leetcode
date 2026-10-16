# 1812. Determine Color of a Chessboard Square

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/determine-color-of-a-chessboard-square/
**Tags:** Math, String

## Approach 1 — 2024-12-23 05:22 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.5 MB*

```java
class Solution {
    public boolean squareIsWhite(String coordinates) {
      char letter=coordinates.charAt(0);
      int digit=coordinates.charAt(1)-'0';

      if(letter=='a'|| letter=='c'|| letter=='e'|| letter=='g'){
        return digit%2==0;
      }else{
        return digit%2==1;
      }
    }
}
```
