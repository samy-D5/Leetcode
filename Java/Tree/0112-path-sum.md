# 112. Path Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/path-sum/
**Tags:** Tree, Depth-First Search, Breadth-First Search, Binary Tree

## Approach 1 — 2026-11-15 14:21 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.4 MB · Time to solve: 39m 52s (timer)*

```java
/**
 * Definition for a binary tree node.
 * public class TreeNode {
 *     int val;
 *     TreeNode left;
 *     TreeNode right;
 *     TreeNode() {}
 *     TreeNode(int val) { this.val = val; }
 *     TreeNode(int val, TreeNode left, TreeNode right) {
 *         this.val = val;
 *         this.left = left;
 *         this.right = right;
 *     }
 * }
 */
class Solution {
    private boolean result;
    public void preorderhelper(TreeNode node, int target, int sum){
        if(node == null) return;
        if(result) return;

        sum+=node.val;

        if(node.left==null && node.right==null){
            if(sum==target){
                result=true;
                return;
            }
        }

        preorderhelper(node.left, target, sum);
        preorderhelper(node.right, target, sum);
    }
    public boolean hasPathSum(TreeNode root, int targetSum) {
        result=false;

        if(root==null) return false;
        preorderhelper(root, targetSum, 0);

        return result;
    }
}
```
