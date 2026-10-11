# 101210. Three Fibonacci Sum

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/three-fibonacci-sum/
**Tags:** 

## Approach 1 — 2026-10-11 08:32 (java)

*Runtime: 2 ms (faster than 25.0%) · Memory: 43 MB · Time to solve: 57m 37s (timer)*

```java
class Solution {
    public boolean threeFibonacciSum(int n) {
        List <Integer> list= fibo(n);
        for(int i=0; i<list.size()-3; i++){
            if(list.get(i)+list.get(i+1)+list.get(i+2) == n) return true;
        }
        return false;
    }
    private ArrayList<Integer> fibo(int n){
        int first=0;
        int second=1;
        int fib=-1;
        ArrayList<Integer> list= new ArrayList<>();
        list.add(first);
        list.add(second);
        while(fib<=n){
            fib=first+second;
            list.add(fib);
            first=second;
            second=fib;
        }
        return list;
    }
}
```
