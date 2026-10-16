# 3190. Find Minimum Operations to Make All Elements Divisible by Three

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-minimum-operations-to-make-all-elements-divisible-by-three/
**Tags:** Array, Math

## Approach 1 — 2024-06-22 21:14 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public int minimumOperations(int[] nums) {
        int count=0;
        for(int i=0;i<nums.length;i++){
            if((nums[i]-1)%3==0) count++;
            else if((nums[i]+1)%3==0) count++;
        }
        return count;
    }
}
```

## Approach 2 — 2025-11-22 23:51 (java)

*Runtime: 1 ms (faster than 22.0%) · Memory: 43.5 MB*

```java
class Solution {
    public int minimumOperations(int[] nums) {
        int res = 0;
        for (int num : nums) {
            if (num % 3 != 0) res++;
        }
        return res;
    }
}
```
