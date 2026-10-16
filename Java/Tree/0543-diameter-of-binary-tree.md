# 543. Diameter of Binary Tree

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/diameter-of-binary-tree/
**Tags:** Tree, Depth-First Search, Binary Tree, DP on Trees

## Approach 1 — 2026-01-13 10:02 (java)

*Runtime: 1 ms (faster than 44.4%) · Memory: 47.1 MB*

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
    int diameter =0;
    public int diameterOfBinaryTree(TreeNode root) {
        height(root);
        return diameter;
    }

    public int height(TreeNode node){
        if(node == null) return 0;
        int l = height(node.left);
        int r = height(node.right);
        diameter = Math.max(diameter, l+r);
        return Math.max(l ,r)+1;
    }
}
```
