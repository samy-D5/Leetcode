# 2652. Sum Multiples

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sum-multiples/
**Tags:** Math

## Approach 1 — 2024-01-29 10:00 (java)

*Runtime: 3 ms (faster than 93.2%) · Memory: 41.1 MB*

```java
class Solution {
    public int sumOfMultiples(int n) {
       int sum=0;
        for(int i=1;i<=n;i++)  if(i%3==0||i%5==0||i%7==0) sum=sum+i;  return sum; }
}
```
