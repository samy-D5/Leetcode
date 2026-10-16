# 328. Odd Even Linked List

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/odd-even-linked-list/
**Tags:** Linked List

## Approach 1 — 2024-07-28 19:52 (java)

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
    public ListNode oddEvenList(ListNode head) {
        ListNode t=head;
        ListNode tempe= new ListNode(0);
        ListNode tempo= new ListNode(0);
        ListNode newHead=tempo;
        ListNode t1=tempe;
        int count=1;
        while(t!=null){
            if(count%2==0){
                tempe.next=t;
                tempe=tempe.next;
            }else{
                tempo.next=t;
                tempo=tempo.next;   
            }
            t=t.next;
            count++;
        }
        tempe.next=null;
        tempo.next=t1.next;
        return newHead.next;
    }
}
```
