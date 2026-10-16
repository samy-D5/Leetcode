# 48. Rotate Image

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/rotate-image/
**Tags:** Array, Math, Matrix

## Approach 1 — 2024-06-17 23:47 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42 MB*

```java
class Solution {
    public void rotate(int[][] matrix) {
    int n=matrix.length;
        for(int i=0;i<n;i++){
            for(int j=i;j<n;j++){
               int temp = matrix[i][j];
				matrix[i][j] = matrix[j][i];
				matrix[j][i] = temp;
            }
        }
        for(int i=0;i<n;i++){
			int low =0;
			int high = n-1;
			while(low <high){
				int temp = matrix[i][low];
				matrix[i][low] = matrix[i][high];
				matrix[i][high] = temp;
				low++;
				high--;
			}
        }

    }
}
```
