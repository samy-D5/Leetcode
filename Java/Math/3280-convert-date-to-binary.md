# 3280. Convert Date to Binary

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/convert-date-to-binary/
**Tags:** Math, String

## Approach 1 — 2024-12-07 00:01 (java)

*Runtime: 8 ms (faster than 6.6%) · Memory: 42.8 MB*

```java
class Solution {
    public String convertDateToBinary(String date) {
        String parts[]=date.split("-");
        int year =Integer.parseInt(parts[0]);
        int month =Integer.parseInt(parts[1]);
        int day =Integer.parseInt(parts[2]);

        String y=Integer.toBinaryString(year);
        String m=Integer.toBinaryString(month);
        String d=Integer.toBinaryString(day);

        return y+"-"+m+"-"+d;
    }
}
```
