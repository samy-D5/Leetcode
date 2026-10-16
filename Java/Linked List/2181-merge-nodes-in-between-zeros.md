# 2181. Merge Nodes in Between Zeros

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/merge-nodes-in-between-zeros/
**Tags:** Linked List, Simulation

## Approach 1 — 2024-08-17 23:58 (java)

*Runtime: 4 ms (faster than 100.0%) · Memory: 80.4 MB*

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
public class Solution {

    public ListNode mergeNodes(ListNode head) {
        ListNode modify = head.next;
        ListNode nextSum = modify;

        while (nextSum != null) {
            int sum = 0;
            while (nextSum.val != 0) {
                sum += nextSum.val;
                nextSum = nextSum.next;
            }

            modify.val = sum;
            nextSum = nextSum.next;
            modify.next = nextSum;
            modify = modify.next;
        }
        return head.next;
    }
}
```

## Approach 2 — 2024-08-23 12:06 (java)

*Runtime: 5 ms (faster than 64.6%) · Memory: 82.1 MB*

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
    public ListNode mergeNodes(ListNode head) {
        ListNode fast= head.next;
        ListNode ans = new ListNode(0);
        ListNode sum=ans;
        for(;fast.next!=null;fast=fast.next){
            if(fast.val==0){ListNode t= new ListNode(0);
            sum.next=t;
            sum=sum.next;}
            else sum.val+=fast.val;
        }
        return ans;
    }
}
```
