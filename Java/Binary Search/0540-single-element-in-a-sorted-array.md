# 540. Single Element in a Sorted Array

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/single-element-in-a-sorted-array/
**Tags:** Array, Binary Search

## Approach 1 — 2024-10-29 18:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 50.6 MB*

```java
class Solution {
    public int singleNonDuplicate(int[] nums) {
        int left = 0, right = nums.length - 1;
        while (left < right) {
            int mid = (left + right) / 2;
            if ((mid % 2 == 0 && nums[mid] == nums[mid + 1]) || (mid % 2 == 1 && nums[mid] == nums[mid - 1]))
                left = mid + 1;
            else
                right = mid;
        }
        return nums[left];
    }
}
```
