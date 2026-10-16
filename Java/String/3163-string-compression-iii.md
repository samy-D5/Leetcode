# 3163. String Compression III

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/string-compression-iii/
**Tags:** String

## Approach 1 — 2024-11-26 00:03 (java)

*Runtime: 17 ms (faster than 92.4%) · Memory: 45.7 MB*

```java
class Solution {
    public String compressedString(String word) {
        StringBuilder comp = new StringBuilder();
        int count=1, n=word.length();
        char ch= word.charAt(0);
        for(int i=1;i<n;i++){
            if(word.charAt(i)==ch && count<9) count++;
            else{
                comp.append(count).append(ch);
                count=1;
                ch=word.charAt(i);
            }
        }
        comp.append(count).append(ch);
        return comp.toString();
    }
}
```

## Approach 2 — 2024-11-26 00:11 (java)

*Runtime: 17 ms (faster than 92.4%) · Memory: 45.8 MB*

```java
class Solution {
    public String compressedString(String word) {
        StringBuilder comp = new StringBuilder();
        int index=0, n=word.length();
        while(index<n){
            int count=0;
            char ch=word.charAt(index);
            while(index<n && word.charAt(index)==ch && count<9){
                count++;
                index++;
            }
            comp.append(count).append(ch);
        }
        return comp.toString();
    }
}
```
