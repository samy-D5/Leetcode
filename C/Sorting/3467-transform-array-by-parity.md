# 3467. Transform Array by Parity

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/transform-array-by-parity/
**Tags:** Array, Sorting, Counting

## Approach 1 — 2025-06-07 18:43 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 12 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* transformArray(int* nums, int numsSize, int* returnSize) {
    int* res = malloc(numsSize*sizeof(int));
    int ind=0;
    for(int i=0; i<numsSize; i++){
        if(nums[i]%2==0) res[ind++]=0;
    }
    
    for(int i=0; i<numsSize; i++){
        if(nums[i]%2!=0) res[ind++]=1;
    }

    *returnSize = numsSize; 
    return res;
}
```

## Approach 2 — 2025-06-19 22:36 (c)

*Runtime: 3 ms (faster than 12.0%) · Memory: 12 MB*

```c
int* transformArray(int* nums, int numsSize, int* returnSize) {
    int* res = malloc(numsSize*sizeof(int));
    int ind=0;
    for(int i=0; i<numsSize; i++){
        if(nums[i]%2==0) res[ind++]=0;
    }
    
    for(int i=0; i<numsSize; i++){
        if(nums[i]%2!=0) res[ind++]=1;
    }

    *returnSize = numsSize; 
    return res;
}
```
