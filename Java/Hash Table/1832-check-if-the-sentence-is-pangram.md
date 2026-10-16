# 1832. Check if the Sentence Is Pangram

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-the-sentence-is-pangram/
**Tags:** Hash Table, String

## Approach 1 — 2025-06-08 16:37 (java)

*Runtime: 1 ms (faster than 85.5%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean checkIfPangram(String s) {
        boolean arr[] = new boolean[26];

        for(char c: s.toCharArray()){
            arr[c - 'a'] = true;
        }

        for(boolean exist: arr){
            if(!exist) return false;
        }
        return true;
    }
}
```

## Approach 2 — 2025-06-08 16:40 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public boolean checkIfPangram(String s) {
       if(s.length()<26) return false;

       for(char ch='a'; ch<='z'; ch++){
        if(s.indexOf(ch)<0) return false;
       }
       return true;
    }
}
```
