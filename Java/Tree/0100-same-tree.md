# 100. Same Tree

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/same-tree/
**Tags:** Tree, Depth-First Search, Breadth-First Search, Binary Tree

## Approach 1 — 2026-11-15 00:59 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.5 MB · Time to solve: 54h 26m (estimated)*

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
    public boolean isSameTree(TreeNode p, TreeNode q) {
        List<TreeNode> one=new ArrayList<>();
        List<TreeNode> two=new ArrayList<>();

        one.add(p);
        two.add(q);

        for(int i=0; i<one.size(); i++){
            TreeNode a = one.get(i);
            TreeNode b = two.get(i);

            if (a==null && b==null) continue;
            if (a==null || b==null) return false;
            if (a.val != b.val) return false;

            one.add(a.left);
            one.add(a.right);
            two.add(b.left);
            two.add(b.right);
        }

        return true;
    }
}
```

**Notes:**

**Time Complexity:** O(N)
**Space Complexity:** O(N)

## Approach 2 — 2026-11-15 13:36 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.8 MB*

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
    public boolean isSameTree(TreeNode p, TreeNode q) {
        List<Integer> one=new ArrayList<>();
        List<Integer> two=new ArrayList<>();

        preorder(p,one);
        preorder(q,two);

        return one.equals(two);
    }

    public void preorder(TreeNode root, List<Integer>list){
        if(root==null){
            list.add(null);
            return;
        }

        list.add(root.val);

        preorder(root.left,list);
        preorder(root.right,list);
    }
}
```
