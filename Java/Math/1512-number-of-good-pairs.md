# 1512. Number of Good Pairs

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-good-pairs/
**Tags:** Array, Hash Table, Math, Counting

## Approach 1 — 2024-05-31 23:59 (java)

*Runtime: 1 ms (faster than 83.4%) · Memory: 40.2 MB*

```java
class Solution {
    public int numIdenticalPairs(int[] nums) {
        int count=0;
        for(int i=0;i<nums.length;i++){
            for(int j=i+1;j<nums.length;j++){
                if(nums[i]==nums[j]) count++;
            }
        }
    return count;
    }
}
```
