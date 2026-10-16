# 283. Move Zeroes

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/move-zeroes/
**Tags:** Array, Two Pointers

## Approach 1 — 2024-09-29 09:51 (java)

*Runtime: 283 ms (faster than 5.2%) · Memory: 46.2 MB*

```java
class Solution {
    public void moveZeroes(int[] nums) {
        for (int i = 0; i < nums.length; i++) {
            for (int j = i+1; j < nums.length; j++) {
                if (nums[i] == 0 && nums[j] != 0) {
                    int temp=0;
                    temp=nums[i];
                    nums[i]=nums[j];
                    nums[j]=temp;
                }
            }

        }
    }
}
```

## Approach 2 — 2024-09-29 13:06 (java)

*Runtime: 1 ms (faster than 99.9%) · Memory: 46.3 MB*

```java
class Solution {
    public void moveZeroes(int[] nums) {
        int n=nums.length;
        int i=0;
        for(int j=0;j<n;j++){
            if(nums[j]!=0){
                nums[i]=nums[j];
                i++;
            }
        }
        // 0 1 0 3 12
        // 1 3 12 _ _
        for(int k=i;k<n;k++) 
            nums[k]=0;
    }   // 1 3 12 _ _
        // 1 3 12 0 0
}
```
