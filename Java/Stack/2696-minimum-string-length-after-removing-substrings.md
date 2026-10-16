# 2696. Minimum String Length After Removing Substrings

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-string-length-after-removing-substrings/
**Tags:** String, Stack, Simulation

## Approach 1 — 2024-10-07 21:58 (java)

*Runtime: 9 ms (faster than 7.8%) · Memory: 44.4 MB*

```java
class Solution {
    public int minLength(String s) {
       while(s.contains("AB") || s.contains("CD")){
        if(s.contains("AB")) s=s.replace("AB","");
        if(s.contains("CD")) s=s.replace("CD","");
       } 
       return s.length();
    }
}
```

## Approach 2 — 2024-10-07 23:18 (java)

*Runtime: 4 ms (faster than 74.2%) · Memory: 42.8 MB*

```java
class Solution {
    public int minLength(String s) {
        int n=s.length();
      Stack<Character> st= new Stack<>();
      //if(n>0) st.push(s.charAt(0));
      for(int i=0;i<n;i++){
        if(!st.isEmpty() && ((s.charAt(i)=='B'&&st.peek()=='A')
        || (s.charAt(i)=='D'&&st.peek()=='C')))
            st.pop();
        else st.push(s.charAt(i));
      }
      return st.size();
    }
}
```
