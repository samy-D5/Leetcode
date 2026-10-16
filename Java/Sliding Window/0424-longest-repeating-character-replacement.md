# 424. Longest Repeating Character Replacement

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/longest-repeating-character-replacement/
**Tags:** Hash Table, String, Sliding Window

## Approach 1 — 2025-06-03 19:34 (java)

*Runtime: 12 ms (faster than 44.1%) · Memory: 44.9 MB*

```java
class Solution {
    public int characterReplacement(String s, int k) {
        int arr[] = new int[26];
        int beg = 0;
        int count=0;
        int maxi = 0;
        for(int i=0;i<s.length(); i++){
            arr[s.charAt(i) - 'A']++;
            count = Math.max(count, arr[s.charAt(i) - 'A']);
            if(i - beg + 1-count > k){
                arr[s.charAt(beg) - 'A']--;
                beg++;
            }
            maxi = Math.max(maxi, i - beg +1);
        }
        return maxi;
    }
}
```
