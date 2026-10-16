# 344. Reverse String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reverse-string/
**Tags:** Two Pointers, String

## Approach 1 — 2024-03-30 10:24 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45.8 MB*

```java
class Solution {
    public void reverseString(char[] s) {
         int left=0;
         int right=s.length-1;
         char temp='a';
         while(left<right){
            temp=s[left];
            s[left]=s[right];
            s[right]=temp;
            left++;
            right--;
         }
    }
}
```

## Approach 2 — 2024-06-02 15:25 (java)

*Runtime: 1 ms (faster than 21.8%) · Memory: 45.5 MB*

```java
class Solution {
    public void reverseString(char[] s) {
         int left=0;
         int right=s.length-1;
         while(left<right){
            s[left]=(char)(s[left]^s[right]);
            s[right]=(char)(s[left]^s[right]);
            s[left]=(char)(s[left]^s[right]);
            left++;
            right--;
         }
    }
}
```
