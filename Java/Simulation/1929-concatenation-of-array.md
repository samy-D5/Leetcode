# 1929. Concatenation of Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/concatenation-of-array/
**Tags:** Array, Simulation

## Approach 1 — 2024-01-16 09:37 (java)

*Runtime: 1 ms (faster than 97.6%) · Memory: 45.2 MB*

```java
class Solution {
    public int[] getConcatenation(int[] nums) {
        int n = nums.length;
        int[]arr=new int[2*n];
        for(int i=0;i<n;i++){
            arr[i]=nums[i];
            arr[n+i]=nums[i];
        }
        return arr;
    }
}
```
