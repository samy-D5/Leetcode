# 2160. Minimum Sum of Four Digit Number After Splitting Digits

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-sum-of-four-digit-number-after-splitting-digits/
**Tags:** Math, Greedy, Sorting

## Approach 1 — 2025-11-19 09:43 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.2 MB*

```java
class Solution {
    public int minimumSum(int num) {
        int max1 = -1, max2 = -1;
        int min1 = 10, min2 = 10;

        while(num>0){
            int digit=num%10;
            if(digit > max1){
                max2= max1;
                max1=digit;
            }else if(digit > max2){
                max2=digit;
            }

            if(min1 > digit){
                min2 =min1;
                min1 = digit;
            }else if(min2 > digit){
                min2=digit;
            }

            num/=10;
        }
        return min1*10 + min2*10 + max1 +max2;
    }
}
```
