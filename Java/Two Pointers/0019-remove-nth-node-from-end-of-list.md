# 19. Remove Nth Node From End of List

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/remove-nth-node-from-end-of-list/
**Tags:** Linked List, Two Pointers

## Approach 1 — 2024-07-20 11:42 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.4 MB*

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
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode temp=head;
        ListNode t=head;
        int count=0;
        while(temp!=null){
            count++;
            temp=temp.next;
        }
        if(count==n) return head.next;
        for(int i=1;i<count-n;i++){
            t=t.next;
        }
        t.next=t.next.next;
        return head;
    }
}
```

## Approach 2 — 2026-09-22 00:42 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.3 MB*

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
    public ListNode removeNthFromEnd(ListNode head, int n) {
        int len=0;
        ListNode cur=head;

        while(cur!=null){
            cur=cur.next;
            len+=1;
        }
        ListNode dummy=new ListNode(0);
        dummy.next=head;

        int jumps = len-n;
        ListNode prev=dummy;

        while(jumps>0){
            prev=prev.next;
            jumps-=1;
        }

        prev.next=prev.next.next;
        return dummy.next;
    }
}
```

## Approach 3 — 2026-09-22 11:13 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.8 MB*

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
    public ListNode removeNthFromEnd(ListNode head, int n) {
        ListNode cur=head;
        int curJumps = n;

        while(curJumps>0){
            cur=cur.next;
            curJumps-=1;
        }
        ListNode dummy=new ListNode(0);
        dummy.next=head;

        ListNode prev=dummy;

        while(cur!=null){
            cur=cur.next;
            prev=prev.next;
        }

        prev.next=prev.next.next;
        return dummy.next;
    }
}
```
