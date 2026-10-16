# 2367. Number of Arithmetic Triplets

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-arithmetic-triplets/
**Tags:** Array, Hash Table, Two Pointers, Enumeration

## Approach 1 — 2025-11-16 00:44 (java)

*Runtime: 17 ms (faster than 32.9%) · Memory: 43.2 MB*

```java
class Solution {
    public int arithmeticTriplets(int[] nums, int diff) {
        int count=0;
        for(int i=0;i<nums.length; i++){
            for(int j=i+1; j<nums.length; j++){
                for(int k=j+1; k<nums.length; k++){
                    if(nums[j]-nums[i]==diff && nums[k]-nums[j]==diff){
                        count++;
                    }
                }
            }
        }
        return count;
    }
}
```

## Approach 2 — 2025-11-16 01:21 (java)

*Runtime: 1 ms (faster than 93.1%) · Memory: 43.6 MB*

```java
class Solution {
    public int arithmeticTriplets(int[] nums, int diff) {
        HashMap<Integer, Integer> seen= new HashMap<>();
        int count=0;
        for(int i=0; i<nums.length; i++) seen.put(nums[i], i);
        for(int num:nums){
            if(seen.containsKey(num+diff) && seen.containsKey(num+2*diff)) count++;
        }
        return count;
    }
}
```
