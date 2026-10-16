# 9. Palindrome Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/palindrome-number/
**Tags:** Math

## Approach 1 — 2024-01-31 13:09 (java)

*Runtime: 4 ms (faster than 100.0%) · Memory: 44.2 MB*

```java
class Solution {
    public boolean isPalindrome(int x) {
       if(x<0){
           return false;
       }
        int temp=x,reverse=0;
        while(temp!=0){
            int digit=temp%10;
            reverse=reverse*10+digit;
            temp/=10;
        }
    return (reverse==x);
    }
}
```

## Approach 2 — 2024-07-18 00:03 (java)

*Runtime: 4 ms (faster than 100.0%) · Memory: 43.8 MB*

```java
class Solution {
    public boolean isPalindrome(int x) {
        if (x<0 || (x!=0 && x%10==0)) return false;
    int rev = 0;
    while (x>rev){
    	rev = rev*10 + x%10;
    	x = x/10;
    }
    return (x==rev || x==rev/10);
    }
}
```
