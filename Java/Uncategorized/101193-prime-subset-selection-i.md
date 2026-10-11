# 101193. Prime Subset Selection I

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/prime-subset-selection-i/
**Tags:** 

## Approach 1 — 2026-10-11 09:29 (java)

*Runtime: 496 ms (faster than 100.0%) · Memory: 48.3 MB · Time to solve: 12s (timer)*

```java
class Solution {
    public List<Integer> maxPrimes(int n, int s) {
        ArrayList<Integer> list=new ArrayList<>();
        int sum=0;
        for(int i=2; i<=n; i++){
            if(isPrime(i)){
                sum+=i;
                if(sum<=s){
                    list.add(i);
                }else break;
            }
        }
        return list;
    }
    boolean isPrime(int n){
       int srt=(int)Math.sqrt(n);
        for(int i=2; i<=srt; i++){
            if(n%i==0) return false;
        }
        return true;
    }

    // boolean[] isPrime(int n){
    //     boolean[] prime=new boolean[n+1];
    //     Arrays.fill(prime,true);

    //     prime[0]=false;
    //     if(n>=1) prime[1]=false;
    //     for(int i=2; i<=n/i)
    // }
}
```
