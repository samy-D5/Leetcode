# 350. Intersection of Two Arrays II

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/intersection-of-two-arrays-ii/
**Tags:** Array, Hash Table, Two Pointers, Binary Search, Sorting

## Approach 1 — 2024-07-08 14:26 (java)

*Runtime: 3 ms (faster than 93.8%) · Memory: 43.2 MB*

```java
class Solution {
    public int[] intersect(int[] nums1, int[] nums2) {
        Arrays.sort(nums1);
        Arrays.sort(nums2);
        int [] ans=new int[Math.min(nums1.length, nums2.length)];
        int i=0,j=0,k=0;
        while(i<nums1.length && j<nums2.length){
            if(nums1[i]<nums2[j]) i++;
            else if(nums1[i]>nums2[j]) j++;
            else{
                ans[k++]=nums1[i];
                i++;
                j++;
            }
        }
        return Arrays.copyOfRange(ans, 0, k);
    }
}
```
