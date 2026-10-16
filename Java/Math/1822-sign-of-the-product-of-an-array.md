# 1822. Sign of the Product of an Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sign-of-the-product-of-an-array/
**Tags:** Array, Math

## Approach 1 — 2024-06-26 19:05 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.7 MB*

```java
class Solution {
    public int arraySign(int[] nums) {
       int negcount=0;
       for(int x:nums){
        if(x==0) return 0;
        if(x<0) negcount++;
       }
    
        return (negcount%2==0)?1:-1;
    }
}
```
