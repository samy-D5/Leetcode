# 2373. Largest Local Values in a Matrix

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/largest-local-values-in-a-matrix/
**Tags:** Array, Matrix

## Approach 1 — 2025-06-08 00:14 (java)

*Runtime: 2 ms (faster than 99.9%) · Memory: 46.1 MB*

```java
class Solution {
    public int[][] largestLocal(int[][] grid) {
        int n = grid.length;
        int[][] arr = new int[n-2][n-2];

        for(int i=0; i<n-2; i++){
            for(int j=0; j<n-2; j++){
                int max=0;
                for(int k=i; k<i+3; k++){
                    for(int l=j; l<j+3; l++){
                        max= Math.max(max, grid[k][l]);
                    }
                }
                arr[i][j]=max;
            }
        }
        return arr;
    }
}
```
