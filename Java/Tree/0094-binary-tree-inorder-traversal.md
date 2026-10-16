# 94. Binary Tree Inorder Traversal

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/binary-tree-inorder-traversal/
**Tags:** Stack, Tree, Depth-First Search, Binary Tree

## Approach 1 — 2026-10-07 01:37 (java)

*Runtime: 0 ms · Memory: 43.2 MB*

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
    public List<Integer> inorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<Integer>();
        Stack<TreeNode> st = new Stack<TreeNode>();
        TreeNode current = root;

        while(current!=null || !st.isEmpty()){
            //reach to the leftmmost node
            while(current!=null){
                st.add(current);
                current = current.left;
            }
            //process node
            current = st.pop();
            list.add(current.val); 
            //visit right subtree
            current = current.right;
        } 
        return list;
    }
}
```
