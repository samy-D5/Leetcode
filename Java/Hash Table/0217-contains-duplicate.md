# 217. Contains Duplicate

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/contains-duplicate/
**Tags:** Array, Hash Table, Sorting

## Approach 1 — 2026-09-01 02:05 (java)

*Runtime: 19 ms (faster than 47.3%) · Memory: 107.8 MB*

```java
class Solution {
    public boolean containsDuplicate(int[] nums) {
        HashSet<Integer> set = new HashSet<>();
        for(int x:nums){
            if(set.contains(x)) return true;
            else set.add(x);
        }
        return false;
    }
}
```
