# 3146. Permutation Difference between Two Strings

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/permutation-difference-between-two-strings/
**Tags:** Hash Table, String

## Approach 1 — 2024-08-13 09:23 (java)

*Runtime: 2 ms (faster than 42.8%) · Memory: 42.6 MB*

```java
class Solution {
    public int findPermutationDifference(String s, String t) {
        int sum=0;
        for(int i=0;i<s.length();i++){
            for(int j=0;j<t.length();j++){
                if(s.charAt(i)==t.charAt(j)) sum+=Math.abs(i-j);
            }
        }
        return sum;
    }
}
```

## Approach 2 — 2024-08-13 09:26 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 42.1 MB*

```java
class Solution {
    public int findPermutationDifference(String s, String t) {
        int sum=0;
        for(int i=0;i<s.length();i++){
           char ch=s.charAt(i);
           int j=t.indexOf(ch);
           sum+=Math.abs(i-j);
        }
        return sum;
    }
}
```

## Approach 3 — 2024-08-29 00:17 (java)

*Runtime: 2 ms (faster than 42.8%) · Memory: 42.7 MB*

```java
class Solution {
    public int findPermutationDifference(String s, String t) {
        int sum=0;
        for(int i=0;i<s.length();i++){
            for(int j=0;j<t.length();j++){
                if(s.charAt(i)==t.charAt(j)){
                    sum+=Math.abs(i-j);
                }
            }
        }
        return sum;
    }
}
```
