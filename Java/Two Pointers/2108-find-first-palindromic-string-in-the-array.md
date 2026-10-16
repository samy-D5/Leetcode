# 2108. Find First Palindromic String in the Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-first-palindromic-string-in-the-array/
**Tags:** Array, Two Pointers, String

## Approach 1 — 2024-03-30 12:10 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 44.6 MB*

```java
class Solution {
    public String firstPalindrome(String[] words) {
        for (int i = 0; i < words.length; i++) {
            int left = 0;
            String str = words[i];
            int right = str.length()- 1;
            boolean check=false;
            
            while (left <= right) {
                if (str.charAt(left) != str.charAt(right)){
                    check = false;
                    break;
                }   
                else
                    check = true;
                    left++;
                    right--;
            }    
                if (check)
                    return str;
            
           
        } return "";
    }
}
```
