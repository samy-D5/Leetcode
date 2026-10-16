# 430. Flatten a Multilevel Doubly Linked List

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/flatten-a-multilevel-doubly-linked-list/
**Tags:** Linked List, Depth-First Search, Doubly-Linked List

## Approach 1 — 2024-08-03 19:38 (java)

*Runtime: 1 ms (faster than 38.8%) · Memory: 41.9 MB*

```java
/*
// Definition for a Node.
class Node {
    public int val;
    public Node prev;
    public Node next;
    public Node child;
};
*/

class Solution {
    public Node flatten(Node head) {
        Node temp=head;
        while(temp!=null){
            Node t=temp.next;
            if(temp.child!=null){
                Node c=flatten(temp.child);
                temp.next=c;
                c.prev=temp;
            while(c.next!=null){
                c=c.next;
            }
            c.next=t;
            if(t!=null) t.prev=c;
            }
            temp.child=null;     
            temp=t;
        }
        return head;
    }
}
```
