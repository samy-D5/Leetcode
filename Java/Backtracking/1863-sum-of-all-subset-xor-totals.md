# 1863. Sum of All Subset XOR Totals

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sum-of-all-subset-xor-totals/
**Tags:** Array, Math, Backtracking, Bit Manipulation, Combinatorics, Enumeration

## Approach 1 — 2026-08-21 23:23 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.8 MB*

```java
class Solution {
    	public int subsetXORSum(int[] nums) {
        return helper(nums, 0, 0);
    }
    
    private int helper(int[] nums, int index, int currentXor) {
        if (index == nums.length) return currentXor;
        
        int withElement = helper(nums, index + 1, currentXor ^ nums[index]);
        
        int withoutElement = helper(nums, index + 1, currentXor);
        
        return withElement + withoutElement;
    }
}
```

## Approach 2 — 2025-09-18 09:33 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.7 MB*

```java
class Solution {
    	public int subsetXORSum(int[] nums) {
        return helper(nums, 0, 0);
    }
    
    private int helper(int[] nums, int index, int currentXor) {
        // return currentXor when all elements in nums are already considered
        if (index == nums.length) return currentXor;
        
        // calculate sum of xor with current element
        int withElement = helper(nums, index + 1, currentXor ^ nums[index]);
        
        // calculate sum of xor without current element
        int withoutElement = helper(nums, index + 1, currentXor);
        
        // return sum of xors from recursion
        return withElement + withoutElement;
    }
}
```
