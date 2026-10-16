# 485. Max Consecutive Ones

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/max-consecutive-ones/
**Tags:** Array

## Approach 1 — 2024-09-29 14:27 (java)

*Runtime: 2 ms (faster than 98.2%) · Memory: 49.9 MB*

```java
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
      int n=nums.length;
      int count=0;
      int max=0;
      for(int i=0;i<n;i++){
        if(nums[i]==1){
            count++;
        }else count=0;
        if(count>max) max=count;
      }  
    return max;
    }
}
```

## Approach 2 — 2026-08-18 10:03 (java)

*Runtime: 2 ms (faster than 98.2%) · Memory: 51.9 MB*

```java
class Solution {
    public int findMaxConsecutiveOnes(int[] nums) {
        int count =0;
        int max=0;
        for(int i=0; i<nums.length; i++){
            if(nums[i]==1) count++;
            else count=0;
            if(count>max) max=count;
        }
        return max;
    }
}
```
