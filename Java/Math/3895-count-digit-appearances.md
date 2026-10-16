# 3895. Count Digit Appearances

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/count-digit-appearances/
**Tags:** Array, Math

## Approach 1 — 2026-04-11 20:12 (java)

*Runtime: 4 ms (faster than 98.0%) · Memory: 47.1 MB*

```java
class Solution {
    public int countDigitOccurrences(int[] nums, int digit) {
        int count =0;
        int num=0;
        for(int i=0; i<nums.length; i++){
      
            while(nums[i]>0){
                num = nums[i]%10;
                if(num==digit) count++;
                nums[i]/=10;
            }
        }
        return count;
    }
}
```
