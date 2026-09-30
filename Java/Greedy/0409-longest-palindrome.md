# 409. Longest Palindrome

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/longest-palindrome/
**Tags:** Hash Table, String, Greedy

## Approach 1 — 2026-09-30 11:13 (java)

*Runtime: 6 ms (faster than 50.5%) · Memory: 43.9 MB*

```java
class Solution {
    public int longestPalindrome(String s) {
        HashSet<Character> h= new HashSet<>();
        int count=0;

        for(char c:s.toCharArray()){
            if(h.contains(c)){
                h.remove(c);
                count+=2;
            }
            else h.add(c);
        }

        if(h.size()>=1) count++;

        return count;
    }
}
```
