# 2325. Decode the Message

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/decode-the-message/
**Tags:** Hash Table, String

## Approach 1 — 2024-08-02 23:36 (java)

*Runtime: 20 ms (faster than 6.3%) · Memory: 45.3 MB*

```java
class Solution {
    public String decodeMessage(String key, String message) {
        int len=key.length();
        String res="";
        ArrayList<Character> noDup = new ArrayList<>();

        for(int i=0;i<len;i++){
            char c=key.charAt(i);
            if(noDup.indexOf(c)==-1 && c!=' ')
                noDup.add(c);
        }
        len=message.length();
        for(int i=0;i<len;i++){
            char c=message.charAt(i);
            if(c==' '){
                res+=" ";
                continue;
            }
            int index=noDup.indexOf(c);
            res+=(char)('a'+index);
        }
        return res;
    }
}
```
