# 26. Remove Duplicates from Sorted Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/remove-duplicates-from-sorted-array/
**Tags:** Array, Two Pointers

## Approach 1 — 2024-09-17 16:28 (java)

*Runtime: 1 ms (faster than 78.4%) · Memory: 44.7 MB*

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        int i=1;
        for (int j=1;j<nums.length;j++) {
            if(nums[j]!=nums[i-1]){
                nums[i]=nums[j];
                i++;
            }
        }
        return i;
    }
}
```

## Approach 2 — 2024-09-17 16:31 (java)

*Runtime: 1 ms (faster than 78.4%) · Memory: 44.5 MB*

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        int i=0;
        for (int j=1;j<nums.length;j++) {
            if(nums[i]!=nums[j]){
                i++;
                nums[i]=nums[j];
            }
        }
        return i+1;
    }
}
```

## Approach 3 — 2025-05-17 23:54 (java)

*Runtime: 1 ms (faster than 78.4%) · Memory: 44.9 MB*

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        if(nums.length == 0) return 0;

        int i=1;
        for(int j=1; j<nums.length;j++){
            if(nums[j]!=nums[i-1]){
                nums[i]=nums[j];
                i++;
            }
        }
        return i;
    }
}
```

## Approach 4 — 2026-08-15 00:10 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 46.7 MB*

```java
class Solution {
    public int removeDuplicates(int[] nums) {
        if(nums.length == 0) return 0;
        int i=1;
        for(int j=1; j<nums.length;j++){
            if(nums[j]!=nums[i-1]){
                nums[i]=nums[j];
                i++;
            }
        }
        return i;
    }
}
```
