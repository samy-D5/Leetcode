# 1903. Largest Odd Number in String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/largest-odd-number-in-string/
**Tags:** Math, String, Greedy

## Approach 1 — 2025-07-17 10:55 (java)

*Runtime: 1 ms (faster than 99.8%) · Memory: 44.8 MB*

```java
class Solution {
    public String largestOddNumber(String num) {
        int i = num.length()-1;
        while(i >= 0){
            int n = num.charAt(i); //Get's ASCII value
            if(n%2 != 0) return num.substring(0, i+1);
            i--;
        }
        return "";
    }
}
```

## Approach 2 — 2025-07-17 10:58 (java)

*Runtime: 1 ms (faster than 99.8%) · Memory: 45 MB*

```java
class Solution {
    public String largestOddNumber(String num) {
        int i = num.length()-1;
        while(i >= 0){
            int n = num.charAt(i) - '0'; // Converst char to int
            if(n%2 != 0) return num.substring(0, i+1);
            i--;
        }
        return "";
    }
}
```
