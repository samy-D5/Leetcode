# 2807. Insert Greatest Common Divisors in Linked List

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/insert-greatest-common-divisors-in-linked-list/
**Tags:** Linked List, Math, Number Theory

## Approach 1 — 2025-06-21 15:26 (java)

*Runtime: 2 ms (faster than 42.9%) · Memory: 45.6 MB*

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
    public ListNode insertGreatestCommonDivisors(ListNode head) {
        if(head.next == null) return head;
        ListNode node1 = head;
        ListNode node2 = head.next;

        while(node2!=null){
            int gcdVal = gcd(node1.val , node2.val);
            ListNode gcdNode = new ListNode(gcdVal);

            node1.next = gcdNode;
            gcdNode.next = node2;

            //move to next pair
            node1 = node2;
            node2 = node2.next;
        }

        return head;
    }

    private int gcd(int a , int b){
        if(b == 0) return a;
        return gcd(b , a%b);
    }
}
```
