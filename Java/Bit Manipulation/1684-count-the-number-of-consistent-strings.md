# 1684. Count the Number of Consistent Strings

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-the-number-of-consistent-strings/
**Tags:** Array, Hash Table, String, Bit Manipulation, Counting

## Approach 1 — 2024-09-04 23:54 (java)

*Runtime: 23 ms (faster than 8.0%) · Memory: 45.4 MB*

```java
class Solution {
    public int countConsistentStrings(String a, String[] w) {
        int count=0;
        for(String s:w){
            boolean valid=true;
            for(char ch:s.toCharArray()){
                if(!a.contains(String.valueOf(ch))) valid=false;
            }
            if(valid) count++;
        }
        return count;
    }
}
```

## Approach 2 — 2024-09-13 01:17 (java)

*Runtime: 5 ms (faster than 96.7%) · Memory: 44.9 MB*

```java
class Solution {
    public int countConsistentStrings(String a, String[] w) {
        int ans[]=new int[26];
        int count=w.length;
        for(char ch:a.toCharArray()){
            ans[ch-'a']++;
           
        }
        for(String str:w){
            for(char ch:str.toCharArray()){
                if(ans[ch-'a']<=0){
                count--;
                break;}
            }
        }
        return count;
    }
}
```
