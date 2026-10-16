# 1688. Count of Matches in Tournament

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-of-matches-in-tournament/
**Tags:** Math, Simulation

## Approach 1 — 2024-01-29 11:01 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.9 MB*

```java
class Solution {
    public int numberOfMatches(int n) {
      int sum=0;
       while(n!=1){
        if(n%2==0){
             sum+=n/2;
             n=n/2;
        }else {
             sum+=(n-1)/2;
             n=(n-1)/2+1;
        }
        
       }
       return sum;
    }
}
```
