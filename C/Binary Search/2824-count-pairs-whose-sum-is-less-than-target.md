# 2824. Count Pairs Whose Sum is Less than Target

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-pairs-whose-sum-is-less-than-target/
**Tags:** Array, Two Pointers, Binary Search, Sorting

## Approach 1 — 2025-06-08 00:22 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.9 MB*

```c
int countPairs(int* nums, int n, int target) {
    int count=0;

    for(int i=0; i<n; i++){
        for(int j=i+1; j<n;j++){
            if(nums[i]+nums[j]<target) count++;
        }
    }
    return count;
}
```
