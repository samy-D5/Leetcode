# 1752. Check if Array Is Sorted and Rotated

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-array-is-sorted-and-rotated/
**Tags:** Array

## Approach 1 — 2024-06-02 14:46 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.9 MB*

```java
class Solution {
    public boolean check(int[] nums) {
        int n = nums.length;
        int count = 0;
        for(int i = 0; i < n-1; i++ )
            if(nums[i] > nums[i+1]) 
                count++;
            
            if(nums[0] < nums[n-1]){
                count++;
            }
                
            return count <=1;
    }
}
```

## Approach 2 — 2024-09-17 16:37 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.4 MB*

```java
class Solution {
    public boolean check(int[] nums) {
        int point1=0;
        int point2=nums.length;
        for(int i=0;i<nums.length;i++){
            if(nums[i]>nums[(i+1)%point2]) point1++;
            if(point1>1) return false;
        }
        return true;
    }
}
```

## Approach 3 — 2025-05-15 08:35 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.1 MB*

```java
class Solution {
    public boolean check(int[] nums) {
        int n = nums.length;
        int count = 0;
        for(int i = 0; i < n-1; i++ )
            if(nums[i] > nums[i+1]) count++;
            if(nums[0] < nums[n-1]) count++;  
        return count <=1;
    }
}
```

## Approach 4 — 2025-05-15 09:21 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean check(int[] nums) {
        int n = nums.length;
        int count = 0;
        for(int i = 0; i < n; i++ ){
            if(nums[i] > nums[(i+1)%n]) count++;  
            if(count>1) return false;
        }
        return true;
    }
}
```

## Approach 5 — 2026-08-05 23:22 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.7 MB*

```java
class Solution {
    public boolean check(int[] nums) {
      int n= nums.length;
      int count=0;
       for(int i=0; i<nums.length; i++){
        if(nums[i] > nums[(i+1)%n]) count++;  
        if(count>1) return false;
       }
       return true;
    }
}
```

## Approach 6 — 2026-08-13 18:08 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.1 MB*

```java
class Solution {
    public boolean check(int[] nums) {
        int n=nums.length;
        int count=0;
        for(int i=0; i<n; i++){
            if(nums[i] > nums[(i+1)%n]){
                count++;
            }
            if(count>1) return false;
        }
        return true;
    }
}
```
