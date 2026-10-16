# 1920. Build Array from Permutation

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/build-array-from-permutation/
**Tags:** Array, Simulation

## Approach 1 — 2024-01-12 12:37 (java)

*Runtime: 1 ms (faster than 99.6%) · Memory: 45.3 MB*

```java
class Solution {
    public int[] buildArray(int[] nums) {
        int n=nums.length;
        int[] arr=new int[n];
        int j;
        for(int i=0;i<n;i++){
            j=nums[i];
            arr[i]=nums[j];
        }
        return arr;
    }
}
```
