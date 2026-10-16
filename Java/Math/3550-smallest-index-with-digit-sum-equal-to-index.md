# 3550. Smallest Index With Digit Sum Equal to Index

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/smallest-index-with-digit-sum-equal-to-index/
**Tags:** Array, Math

## Approach 1 — 2025-09-23 23:07 (java)

*Runtime: 1 ms (faster than 99.6%) · Memory: 44.4 MB*

```java
class Solution {
    public int smallestIndex(int[] nums) {
        // int index=-1;
        for(int i=0;i<nums.length;i++){
            if(digitSum(nums[i]) == i){
                return i;
            }
        }

       return -1; 
    }

    private static int digitSum(int n){
        int s =0;
        while(n>0){
            int digit =n%10;
            s +=digit;
            n/=10;
        }
        return s;
    }
}
```
