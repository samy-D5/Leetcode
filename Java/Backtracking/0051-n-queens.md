# 51. N-Queens

**Difficulty:** Hard
**Link:** https://leetcode.com/problems/n-queens/
**Tags:** Array, Backtracking, Algorithm X

## Approach 1 — 2025-12-02 21:55 (java)

*Runtime: 1 ms (faster than 99.8%) · Memory: 46.6 MB*

```java
class Solution {
    public List<List<String>> solveNQueens(int n) {
        List<List<String>> res = new ArrayList<>();
        char[][] board = new char[n][n];
        for(int i=0; i<n; i++) Arrays.fill(board[i], '.');

        boolean[] col= new boolean[n];
        boolean[] dia1= new boolean[2*n-1]; //row-col+n
        boolean[] dia2= new boolean[2*n-1]; //row+col

        backtrack(0, n ,board, col, dia1, dia2, res);
        return res;
    }

    private void backtrack(int row, int n, char[][] board, boolean[]col, boolean[]dia1, boolean[]dia2, List<List<String>>res){
        if(row==n){
            List<String> curr=new ArrayList<>();
            for(int i=0; i<n; i++) curr.add(new String(board[i]));
            res.add(curr);

            return;
        }

        for(int c=0; c<n; c++){
            int d1=row-c+n-1;
            int d2= row + c;

            if(!col[c] && !dia1[d1] && !dia2[d2]){
                col[c]= dia1[d1] = dia2[d2] = true;
                board[row][c] = 'Q';

                backtrack(row+1, n, board, col, dia1, dia2, res);

                board[row][c] = '.';
                col[c] = dia1[d1] = dia2[d2] = false;
            }
        }
    }
}
```
