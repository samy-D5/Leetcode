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

## Approach 2 — 2026-09-29 20:22 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 46.9 MB*

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
        ListNode fast = head;
        ListNode slow = head;
        while(fast!=null && fast.next!=null){
            slow=slow.next;
            fast=fast.next.next;
            if(slow==fast) return true;
        }
        return false;
    }
}
```

**Notes:**

# Floyd's cycle Finding Algorithm 
*OR*
# Tortoise & Heir Algorithm
**TC** : O(1)
**SC** : O(n)

