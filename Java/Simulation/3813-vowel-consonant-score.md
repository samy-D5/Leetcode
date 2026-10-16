# 3813. Vowel-Consonant Score

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/vowel-consonant-score/
**Tags:** String, Simulation

## Approach 1 — 2026-01-18 08:18 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 43.8 MB*

```java
class Solution {
    public int vowelConsonantScore(String s) {
        int v=0;
        int c=0;
        int score=0;
        for(int i=0; i<s.length(); i++){
            int ch= s.charAt(i);
            if(ch=='a'||ch=='e'||ch=='i'||ch=='o'||ch=='u'){
                v++;
            }else if(Character.isDigit(ch) || Character.isWhitespace(ch)){
                continue;
            }else c++;
        }
        if(c==0) return 0;
        score=(v/c);
        return score;
    }
}
```
