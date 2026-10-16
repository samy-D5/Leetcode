# 2415. Reverse Odd Levels of Binary Tree

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/reverse-odd-levels-of-binary-tree/
**Tags:** Tree, Depth-First Search, Breadth-First Search, Binary Tree

## Approach 1 — 2026-01-13 08:55 (java)

*Runtime: 1 ms (faster than 91.4%) · Memory: 49.7 MB*

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
    public TreeNode reverseOddLevels(TreeNode root) {
       traverse(root.left, root.right, 1);
       return root;
    }

    public void traverse(TreeNode node1, TreeNode node2, int lvl){
        if(node1==null || node2 == null) return;
        if(lvl%2==1){
            int temp = node1.val;
            node1.val = node2.val;
            node2.val = temp;
        }
        traverse(node1.left, node2.right, lvl+1);
        traverse(node1.right, node2.left, lvl+1);
    }
}
```
