# 2520. Count the Digits That Divide a Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-the-digits-that-divide-a-number/
**Tags:** Math

## Approach 1 — 2024-01-30 20:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.5 MB*

```java
class Solution {
    public int countDigits(int num) {
        int count=0;
         int n=num;
          while(num!=0)
          {
              int v=num%10;
              if(n%v==0){
                   count++;
              }
              num=num/10;
          }
        return count; 
    }
}
```
