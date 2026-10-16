# 21. Merge Two Sorted Lists

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/merge-two-sorted-lists/
**Tags:** Linked List, Recursion

## Approach 1 — 2024-07-27 23:16 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.5 MB*

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
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        ListNode temp1=list1;
        ListNode temp2=list2;
        ListNode temp=new ListNode(100);
        ListNode head=temp;
        while(temp1!=null && temp2!=null ){
            if(temp1.val<=temp2.val){
               temp.next=temp1;
               temp=temp.next;
               temp1=temp1.next;
            }
            else{
               temp.next=temp2;
               temp=temp.next;
               temp2=temp2.next;
            }
        }if(temp1==null) temp.next=temp2;
            else temp.next=temp1;
        return head.next;
    }
}
```

## Approach 2 — 2025-10-27 23:25 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.4 MB*

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
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        ListNode dummy = new ListNode(-1);
        ListNode curr = dummy;

        while(list1 != null && list2!=null){
            if(list1.val <= list2.val){
                curr.next = list1;
                list1 = list1.next;
            } else {
                curr.next = list2;
                list2 = list2.next;
            }
            curr = curr.next;
        }

        curr.next = (list1!=null) ? list1 : list2;

        return dummy.next;
        
    }
}
```

## Approach 3 — 2025-10-29 09:16 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.5 MB*

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
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        if(list1 == null || list2 == null) { //base case
            return (list1!=null) ? list1 : list2;
        }

        if(list1.val > list2.val){ // swap head if list2 is smaller than list1
           ListNode temp = list1;
           list1 = list2;
           list2 = temp;
        }

        list1.next = mergeTwoLists(list1.next, list2); // compare the smaller head with the next one with recurrsion.
        return list1; 
    }
}
```

## Approach 4 — 2026-09-23 23:30 (java)

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
    public ListNode mergeTwoLists(ListNode list1, ListNode list2) {
        ListNode dummy=new ListNode(0);
        ListNode curr=dummy;

        while(list1!=null && list2!=null){
            if(list1.val<list2.val){
                curr.next=list1;
                curr=list1;
                list1=list1.next;
            }else{
                curr.next=list2;
                curr=list2;
                list2=list2.next;
            }
        }
        if(list1==null) curr.next=list2;
        else curr.next=list1;

        return dummy.next;


    }
}
```
