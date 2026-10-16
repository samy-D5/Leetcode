# 2894. Divisible and Non-divisible Sums Difference

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/divisible-and-non-divisible-sums-difference/
**Tags:** Math

## Approach 1 — 2024-01-27 16:43 (java)

*Runtime: 1 ms (faster than 92.6%) · Memory: 40.7 MB*

```java
class Solution {
    public int differenceOfSums(int n, int m) {
        int sum1=0;
        int sum2=0;
        for(int i=1;i<=n;i++){
            if(i%m==0){
                sum1+=i;
            }else{
                sum2+=i;
            }
           
        }
        return  sum2-sum1;
    }
}
```
