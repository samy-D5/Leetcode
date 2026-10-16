# 3304. Find the K-th Character in String Game I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-the-k-th-character-in-string-game-i/
**Tags:** Math, Bit Manipulation, Recursion, Simulation

## Approach 1 — 2025-09-25 22:31 (java)

*Runtime: 3 ms (faster than 63.5%) · Memory: 41.6 MB*

```java
class Solution {
    public char kthCharacter(int k) {
        StringBuilder builder = new StringBuilder("a");

        while(builder.length() < k){
            int size = builder.length();
            for(int i=0; i<size; i++)
                builder.append((char)('a'+((builder.charAt(i)-'a')+1)%26));
        }
        return builder.charAt(k-1);
    }
}
```
