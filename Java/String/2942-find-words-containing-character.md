# 2942. Find Words Containing Character

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-words-containing-character/
**Tags:** Array, String

## Approach 1 — 2024-06-25 12:02 (java)

*Runtime: 2 ms (faster than 44.2%) · Memory: 44.7 MB*

```java
class Solution {
    public List<Integer> findWordsContaining(String[] words, char x) {
        ArrayList<Integer> list=new ArrayList<>();
        for(int i=0;i<words.length;i++){
            for(int j=0;j<words[i].length();j++){
                if(x==words[i].charAt(j)){
                    list.add(i);
                    break;
                }
            }
        }
        return list;
    }
}
```
