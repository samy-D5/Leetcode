# 3516. Find Closest Person

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-closest-person/
**Tags:** Math

## Approach 1 — 2025-09-18 22:08 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.6 MB*

```java
class Solution {
    public int findClosest(int x, int y, int z) {
        int one= Math.abs(z-x);
        int two = Math.abs(z-y);

        if(one>two) return 2;
        else if(one<two) return 1;
        else return 0;
    }
}
```
