# 2418. Sort the People

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sort-the-people/
**Tags:** Array, Hash Table, String, Sorting

## Approach 1 — 2024-07-22 23:36 (java)

*Runtime: 5 ms (faster than 99.3%) · Memory: 45.4 MB*

```java
class Solution {
    public String[] sortPeople(String[] names, int[] heights) {
        String[] res = new String[names.length];
        int[] index = new int[100001];
        for(int i=0;i<heights.length;i++)
            index[heights[i]] = i;
        Arrays.sort(heights);
        for(int i = 0; i < heights.length; i++)
            res[heights.length - i - 1] = names[index[heights[i]]];
        return res;
    }
}
```
