# 3. Longest Substring Without Repeating Characters

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/longest-substring-without-repeating-characters/
**Tags:** Hash Table, String, Sliding Window

## Approach 1 — 2026-09-29 13:06 (java)

```java
class Solution {
    public int lengthOfLongestSubstring(String s) {
        int count = 0;

        if(s.length()<=1) return s.length();
        for(int i=0; i<s.length(); i++){
            HashSet<Character> set = new HashSet<>();
            for(int j=i; j<s.length(); j++){
                if(set.contains(s.charAt(j))){
                    count = Math.max(count, j-i);
                    break;
                }
                set.add(s.charAt(j));
            }
            count = Math.max(count, set.size());
        }
        return count;
    }
}
```
