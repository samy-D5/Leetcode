# 3921. Score Validator

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/score-validator/
**Tags:** Array, String, Simulation

## Approach 1 — 2026-05-09 20:29 (java)

*Runtime: 17 ms (faster than 5.0%) · Memory: 47.9 MB*

```java
class Solution {
    public int[] scoreValidator(String[] events) {
        int score = 0;
        int counter=0;

        for(String x: events){
            if(counter>=10) break;
            else if(x.matches("[0-6]")) score += Integer.parseInt(x);
            else if(x.equals("W")) counter++;
            else if(x.equals("WD") || x.equals("NB")) score++;
        }
        return new int[]{score,counter};
    }
}
```
