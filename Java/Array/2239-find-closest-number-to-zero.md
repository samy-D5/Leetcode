# 2239. Find Closest Number to Zero

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-closest-number-to-zero/
**Tags:** Array

## Approach 1 — 2024-10-30 15:10 (java)

*Runtime: 2 ms (faster than 84.7%) · Memory: 44.8 MB*

```java
class Solution {
    public int findClosestNumber(int[] nums) {
        int max=Integer.MAX_VALUE;
        int ans=0;
        for(int i:nums){
            if(Math.abs(i)<max){
                max=Math.abs(i);
                ans=i;
            }else if(Math.abs(i)==max)
                ans=Math.max(ans,i);
        }
        return ans;
    }
}
```

## Approach 2 — 2024-10-30 15:16 (java)

*Runtime: 2 ms (faster than 84.7%) · Memory: 44.6 MB*

```java
class Solution {
    public int findClosestNumber(int[] nums) {
        int min=Integer.MAX_VALUE;
        int ans=0;
        for(int i:nums){
            if(Math.abs(i)<min){
                min=Math.abs(i);
                ans=i;
            }else if(Math.abs(i)==min)
                ans=Math.max(ans,i);
        }
        return ans;
    }
}
```
