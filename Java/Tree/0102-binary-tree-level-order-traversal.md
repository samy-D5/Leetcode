# 102. Binary Tree Level Order Traversal

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/binary-tree-level-order-traversal/
**Tags:** Tree, Breadth-First Search, Binary Tree

## Approach 1 — 2026-11-13 00:48 (java)

*Runtime: 1 ms (faster than 97.9%) · Memory: 46.3 MB · Time to solve: 14m 57s (timer)*

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
    public List<List<Integer>> levelOrder(TreeNode root) {
        List<List<Integer>> ans = new ArrayList<>();
        pre(root, 0, ans);
        return ans;
    }

    public static void pre(TreeNode root, int level, List<List<Integer>>ans){
        if(root==null) return;
        if(ans.size()==level){
            List<Integer> list=new ArrayList<>();
            list.add(root.val);
            ans.add(list);
        }else {
            ans.get(level).add(root.val);
        }
        pre(root.left, level+1, ans);
        pre(root.right, level+1, ans);
    }
}
```
