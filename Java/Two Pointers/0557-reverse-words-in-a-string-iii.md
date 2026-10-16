# 557. Reverse Words in a String III

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reverse-words-in-a-string-iii/
**Tags:** Two Pointers, String

## Approach 1 — 2025-06-09 12:20 (java)

*Runtime: 3 ms (faster than 99.4%) · Memory: 45.3 MB*

```java
class Solution {
    public String reverseWords(String s) {
        char ch[] = s.toCharArray();

        for(int i=0; i<ch.length; i++){
            if(ch[i]!= ' '){
                int j = i;
                while(j+1<ch.length && ch[j+1]!= ' ') j++;
                reverse(ch , i ,j);
                i = j;
            }
        }
        return new String(ch);
    }
     
    private void reverse(char[]ch , int i, int j ){
        for(;i<j; i++, j--){
            char temp = ch[i];
            ch[i] = ch[j];
            ch[j] = temp;
        }
    }
}
```
