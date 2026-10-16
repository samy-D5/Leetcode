# 3264. Final Array State After K Multiplication Operations I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/final-array-state-after-k-multiplication-operations-i/
**Tags:** Array, Math, Heap (Priority Queue), Simulation

## Approach 1 — 2025-06-08 00:50 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 12.2 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* getFinalState(int* nums, int n, int k, int multiplier, int* returnSize) {
    int* arr = malloc(n*sizeof(int));

    for(int i=0; i<n; i++) arr[i]=nums[i];
    
    for(int j=0; j<k; j++){
        int minInd=0;
        for(int i=1; i<n; i++){
            if(arr[i]<arr[minInd]) minInd=i;   
        }
        arr[minInd] *= multiplier;
    }

    *returnSize = n;
    return arr;
}
```
