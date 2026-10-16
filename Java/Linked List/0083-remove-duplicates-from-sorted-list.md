# 83. Remove Duplicates from Sorted List

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/remove-duplicates-from-sorted-list/
**Tags:** Linked List

## Approach 1 — 2024-07-28 10:44 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.2 MB*

```java
/**
 * Definition for singly-linked list.
 * public class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode() {}
 *     ListNode(int val) { this.val = val; }
 *     ListNode(int val, ListNode next) { this.val = val; this.next = next; }
 * }
 */
class Solution {
    public ListNode deleteDuplicates(ListNode head) {
        ListNode temp=head;
        ListNode last=head;
        if(head==null) return head;
        while(temp!=null){
         if(temp.val!=last.val){
           last.next=temp;
           last=temp;
          }
          temp=temp.next;
        }
        last.next=null;
        return head;
    }
}
```
