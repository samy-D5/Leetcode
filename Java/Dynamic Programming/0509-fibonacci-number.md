# 509. Fibonacci Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/fibonacci-number/
**Tags:** Math, Dynamic Programming, Recursion, Memoization

## Approach 1 — 2025-05-15 07:45 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.7 MB*

```java
class Solution {
    public int fib(int n) {
        if(n<=1) return n;
        int a=0, b=1, sum=0;
        for(int i=2;i<=n;i++) {
            sum = a+b;
            a=b;
            b=sum;
        }
        return sum;
        
    }
}
```

## Approach 2 — 2025-05-15 07:46 (java)

*Runtime: 8 ms (faster than 43.0%) · Memory: 40.2 MB*

```java
class Solution {
    public int fib(int n) {
        if(n ==0 || n ==1) return n;
        return fib(n-1)+fib(n-2);        
    }
}
```
