# 3736. Minimum Moves to Equal Array Elements III

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-moves-to-equal-array-elements-iii/
**Tags:** Array, Math

## Approach 1 — 2025-11-08 20:15 (java)

*Runtime: 2 ms (faster than 19.5%) · Memory: 46.5 MB*

```java
class Solution {
    public int minMoves(int[] nums) {
        int max=nums[0];
        for(int i=0; i<nums.length; i++){
            max= Math.max(max, nums[i]);
        }
        int count=0;
        for(int i=0; i<nums.length; i++){
            while(nums[i]<max){
                nums[i]++;
                count++;
            }
        }
        return count;
    }
}
```
