# 3151. Special Array I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/special-array-i/
**Tags:** Array

## Approach 1 — 2025-02-09 20:26 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.5 MB*

```java
class Solution {
    public boolean isArraySpecial(int[] nums) {
        if(nums.length==1) return true; 
        for(int i=0;i<nums.length-1;i++){
            if(nums[i]%2==0){
                if(nums[(i+1)]%2==0) return false;
            }
            else if(nums[i]%2!=0){
                if(nums[(i+1)]%2!=0) return false;
            }
        }
        return true;
    }
}
```
