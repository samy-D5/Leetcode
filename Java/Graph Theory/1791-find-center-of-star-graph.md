# 1791. Find Center of Star Graph

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-center-of-star-graph/
**Tags:** Graph Theory

## Approach 1 — 2024-06-28 23:02 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 66.7 MB*

```java
class Solution {
    public int findCenter(int[][] edges) {
        int ans=0;
        int a=edges[0][0];
        int b=edges[0][1];
        if (a == edges[1][0] || a == edges[1][1])
            return a;
         else 
            return b;
    }
}
```

## Approach 2 — 2024-07-02 23:35 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 66.6 MB*

```java
class Solution {
    public int findCenter(int[][] e) {
     return e[0][0] == e[1][0] || e[0][0] == e[1][1] ? e[0][0] : e[0][1];

    }
}
```
