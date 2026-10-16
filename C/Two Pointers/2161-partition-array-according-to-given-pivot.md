# 2161. Partition Array According to Given Pivot

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/partition-array-according-to-given-pivot/
**Tags:** Array, Two Pointers, Simulation

## Approach 1 — 2025-06-07 18:35 (c)

*Runtime: 9 ms (faster than 22.9%) · Memory: 98.5 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
#include <stdlib.h>
int* pivotArray(int* nums, int numsSize, int pivot, int* returnSize) {
    int* result = malloc(numsSize*sizeof(int));
    int ind1=0, ind2=numsSize - 1;
    
    for(int i=0; i<numsSize; i++){
        if(nums[i]<pivot) result[ind1++] = nums[i];
    }

    for(int i=numsSize-1; i>=0; i--){
        if(nums[i]>pivot) result[ind2--]=nums[i];
    }

    while(ind1<=ind2){
        result[ind1++]=pivot;
    }

    *returnSize = numsSize;
    return result;
}
```

## Approach 2 — 2025-06-07 18:36 (c)

*Runtime: 9 ms (faster than 22.9%) · Memory: 98.3 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
#include <stdlib.h>
int* pivotArray(int* nums, int numsSize, int pivot, int* returnSize) {
    int* result = malloc(numsSize*sizeof(int));
    int ind1=0;
    
    for(int i=0; i<numsSize; i++){
        if(nums[i]<pivot) result[ind1++] = nums[i];
    }

    for(int i=0;i<numsSize;i++){
        if(nums[i]==pivot) result[ind1++]=nums[i];
    }

    for(int i=0;i<numsSize;i++){
        if(nums[i]>pivot) result[ind1++]=nums[i];
    }

    *returnSize = numsSize;
    return result;
}
```
