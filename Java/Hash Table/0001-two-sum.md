# 1. Two Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/two-sum/
**Tags:** Array, Hash Table

## Approach 1 — 2024-01-31 12:44 (java)

*Runtime: 44 ms (faster than 33.9%) · Memory: 45.3 MB*

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
       for(int i=0;i<nums.length;i++){
           for(int j=i+1;j<nums.length;j++){
               if(nums[i]+nums[j]==target){
               int arr[]={i,j};
               return arr;
               }
           }
       } 
       return null;
    }
}
```

## Approach 2 — 2024-07-01 16:34 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.5 MB*

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
        for (int i=1; i < nums.length; i++) {
            for (int j=i; j < nums.length; j++) {
                if (nums[j]+nums[j - i] == target){
                    return new int[] {j, j - i};
                }
            }
        }
        return null;
    }
}
```

## Approach 3 — 2024-07-01 21:02 (java)

*Runtime: 2 ms (faster than 99.4%) · Memory: 45 MB*

```java
class Solution {
        public int[] twoSum(int[] nums, int target) {
                Map<Integer, Integer> pairIdx = new HashMap<>();

                        for (int i = 0; i < nums.length; i++) {
                                    int num = nums[i];
                                                if (pairIdx.containsKey(target - num)) {
                                                                return new int[] { i, pairIdx.get(target - num) };
                                                                            }
                                                                                        pairIdx.put(num, i);
                                                                                                }

                                                                                                        return new int[] {};        
                                                                                                            }
                                                                                                            }
```

## Approach 4 — 2024-10-15 23:59 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.9 MB*

```java
class Solution {
    public int[] twoSum(int[] nums, int target) {
     for(int i=1;i<nums.length;i++){
        for(int j=i;j<nums.length;j++){
            int a=j-i;
            if(nums[a]+nums[j]==target)return new int[]{a,j};
        }
     }
    return new int[] {0};
    }
}
```
