# 1720. Decode XORed Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/decode-xored-array/
**Tags:** Array, Bit Manipulation

## Approach 1 — 2025-06-08 01:06 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 25.1 MB*

```c
/**
 * Note: The returned array must be malloced, assume caller calls free().
 */
int* decode(int* encoded, int n, int first, int* returnSize) {
    *returnSize=n+1;
    int* arr= (int*)malloc(*returnSize*sizeof(int));
    arr[0]=first;

    for(int i=0; i<n; i++){
       arr[i+1]=arr[i]^encoded[i];
    }
    return arr;
}
```
