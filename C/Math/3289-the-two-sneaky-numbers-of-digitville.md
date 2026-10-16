# 3289. The Two Sneaky Numbers of Digitville

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/the-two-sneaky-numbers-of-digitville/
**Tags:** Array, Hash Table, Math

## Approach 1 — 2025-06-07 19:02 (c)

*Runtime: 3 ms (faster than 15.5%) · Memory: 10.2 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* getSneakyNumbers(int* nums, int numsSize, int* returnSize) {
    int* arr = malloc(numsSize*sizeof(int));
    int ind=0;

    for(int i=0; i<numsSize; i++){
        for(int j=i+1; j<numsSize; j++){
            if(nums[i]==nums[j]) arr[ind++]=nums[j];
        }
    }

    *returnSize = ind;
    return arr;
}
```
