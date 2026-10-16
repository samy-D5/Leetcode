# 2544. Alternating Digit Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/alternating-digit-sum/
**Tags:** Math

## Approach 1 — 2024-06-26 20:00 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40 MB*

```java
class Solution {
    public int alternateDigitSum(int n) {
       int sum=0;
       int count=0;
       boolean check=false;
       int num=n;
       while(num>0){
         num/=10;
         count++;
       } 
       if(count%2==0)
            check=true;
       while(n>0){
        if(check==false)
                 sum+=n%10;
        else if(check==true)
                sum-=n%10;
        n/=10;
        check=!check;
       }
    return sum;
    }
}
```
