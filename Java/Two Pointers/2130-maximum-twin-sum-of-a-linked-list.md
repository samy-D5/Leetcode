# 2130. Maximum Twin Sum of a Linked List

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/maximum-twin-sum-of-a-linked-list/
**Tags:** Linked List, Two Pointers, Stack

## Approach 1 — 2024-07-28 17:12 (java)

*Runtime: 8 ms (faster than 28.3%) · Memory: 67.2 MB*

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
    public int pairSum(ListNode head) {
        ListNode slow=head;
        ListNode fast=head;
        while(fast.next!=null && fast.next.next!=null){
            slow=slow.next;
            fast=fast.next.next;
        }
        ListNode mid=slow;
        ListNode t1=head;
        mid.next=reverse(mid.next);
        ListNode t2=mid.next;
        int sum=0;
        while(t2!=null){
            sum=Math.max(sum, t1.val+t2.val);
            t1=t1.next;
            t2=t2.next;
        }
        return sum;
    }
    public ListNode reverse(ListNode head){
        if(head==null) return null;
        if(head.next==null) return head;
        ListNode newHead = reverse(head.next);
        head.next.next=head;
        head.next=null;
        return newHead;
    }
}
```
