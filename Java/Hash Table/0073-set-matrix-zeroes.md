# 73. Set Matrix Zeroes

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/set-matrix-zeroes/
**Tags:** Array, Hash Table, Matrix

## Approach 1 — 2025-05-12 22:38 (java)

*Runtime: 1 ms (faster than 95.8%) · Memory: 45.5 MB*

```java
class Solution {
    public void setZeroes(int[][] matrix) {
        int rows = matrix.length;
        int cols = matrix[0].length;

        for(int i=0; i<rows; i++){
            for(int j=0; j<cols; j++){
                if(matrix[i][j]==0){
                    //make rows -1
                    for(int m=0;m<rows;m++) {
                        if(matrix[m][j]!=0) matrix[m][j]=-100000;
                    }
                    //make cols -1
                    for(int n=0;n<cols;n++) {
                        if(matrix[i][n]!=0) matrix[i][n]=-100000;
                    }
                }
            }
        }
        // make -1 to 0
        for(int i=0;i<rows;i++) {
            for(int j=0;j<cols;j++){
                if(matrix[i][j]==-100000) matrix[i][j]=0;
            }
        }
    }
}
```
