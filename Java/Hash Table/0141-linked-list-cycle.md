# 141. Linked List Cycle

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/linked-list-cycle/
**Tags:** Hash Table, Linked List, Two Pointers, Floyd's Cycle Finding Algorithm

## Approach 1 — 2026-09-29 19:51 (java)

*Runtime: 7 ms (faster than 8.4%) · Memory: 46.6 MB*

```java
/**
 * Definition for singly-linked list.
 * class ListNode {
 *     int val;
 *     ListNode next;
 *     ListNode(int x) {
 *         val = x;
 *         next = null;
 *     }
 * }
 */
public class Solution {
    public boolean hasCycle(ListNode head) {
        ListNode curr = head;
        Set<ListNode> set = new HashSet<>();
        while(curr!=null){
            if(set.contains(curr)){
                return true;
            }
            set.add(curr);
            curr=curr.next;
        }
        return false;
    }
}
```

**Notes:**

**Time Complexity:** O(n)
**Space Complexity:** O(n)

