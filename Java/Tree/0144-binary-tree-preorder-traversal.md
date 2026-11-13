# 144. Binary Tree Preorder Traversal

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/binary-tree-preorder-traversal/
**Tags:** Stack, Tree, Depth-First Search, Binary Tree

## Approach 1 — 2026-11-13 14:02 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.9 MB · Time to solve: 19m 33s (timer)*

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
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> ans = new ArrayList<>();
        Stack<TreeNode> stack = new Stack<>();
        if(root==null) return ans;
        stack.add(root);

        while(!stack.isEmpty()){
            TreeNode node = stack.pop();

            ans.add(node.val);

            if(node.right!=null) stack.add(node.right);
            if(node.left!=null) stack.add(node.left);
        }
        return ans; 
    }

}
```

## Approach 2 — 2026-11-13 14:18 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.6 MB · Time to solve: 8m 9s (estimated)*

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
    public List<Integer> preorderTraversal(TreeNode root) {
        List<Integer> list = new ArrayList<>();
        return recursion(root, list);
    }

    public List<Integer> recursion(TreeNode root, List<Integer> list){
        if(root==null) return list;
        list.add(root.val);
        recursion(root.left,list);
        recursion(root.right,list);
        return list;
    }
}
```
