# 559. Maximum Depth of N-ary Tree

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-depth-of-n-ary-tree/
**Tags:** Tree, Depth-First Search, Breadth-First Search

## Approach 1 — 2026-01-12 22:21 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45.2 MB*

```java
/*
// Definition for a Node.
class Node {
    public int val;
    public List<Node> children;

    public Node() {}

    public Node(int _val) {
        val = _val;
    }

    public Node(int _val, List<Node> _children) {
        val = _val;
        children = _children;
    }
};
*/

class Solution {
    public int maxDepth(Node root) {
        if(root == null) return 0;
        int max=1;
        for(int i=0; i<root.children.size(); i++){
            max = Math.max(max, 1+maxDepth(root.children.get(i)));
        }
        return max;
    }
}
```
