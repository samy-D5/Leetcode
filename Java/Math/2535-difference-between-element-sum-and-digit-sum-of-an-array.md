# 2535. Difference Between Element Sum and Digit Sum of an Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/difference-between-element-sum-and-digit-sum-of-an-array/
**Tags:** Array, Math

## Approach 1 — 2024-01-28 23:17 (java)

*Runtime: 2 ms (faster than 99.2%) · Memory: 44.9 MB*

```java
class Solution {
    public int differenceOfSum(int[] nums) {
        int esum=0,dsum=0;
        for(int i=0;i<nums.length;i++){
            esum+=nums[i];
        
        while(nums[i]>0){
            int rem=nums[i]%10;
            dsum+=rem;
            nums[i]=nums[i]/10;
        }
        }
        return esum-dsum;

    }
}
```

## Approach 2 — 2024-06-08 23:15 (java)

*Runtime: 2 ms (faster than 99.2%) · Memory: 44.9 MB*

```java
class Solution {
    public int differenceOfSum(int[] nums) {
        int element_sum = 0;
        int digit_sum = 0;
        for(int i=0;i<nums.length;i++){
            element_sum+=nums[i];

            int val = nums[i];
            int x;
            
            while(val>0){
                x = val%10;
                digit_sum +=x;
                val = val/10;
            }
        }
        return Math.abs(element_sum - digit_sum);
    }
}
```
