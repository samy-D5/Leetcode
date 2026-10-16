# 234. Palindrome Linked List

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/palindrome-linked-list/
**Tags:** Linked List, Two Pointers, Stack, Recursion

## Approach 1 — 2026-09-29 12:08 (java)

*Runtime: 7 ms (faster than 27.3%) · Memory: 99.7 MB*

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
    public boolean isPalindrome(ListNode head) {
       ArrayList<Integer> list = new ArrayList<>();
        ListNode curr = head;

        while(curr !=null){
            list.add(curr.val);
            curr=curr.next;
        }

        int p1=0;
        int p2=list.size()-1;

        while(p1<p2){
            if(list.get(p1)!=list.get(p2)) return false;
            p1++;
            p2--;
        }
        return true;
    }
}
```
