# 7. Reverse Integer

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/reverse-integer/
**Tags:** Math

## Approach 1 — 2024-04-14 21:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.6 MB*

```java
class Solution {
    public int reverse(int x) {
        int temp=0;
        long ans=0;
        while (x != 0){
            temp=x%10;
            ans=(10*ans)+temp; 
            x/=10;
        }
        if(ans> Integer.MAX_VALUE || ans<Integer.MIN_VALUE){
            return 0;
        }
        if(x<0) return (int)(-1*ans);
        return (int)ans;
    }
}
```

## Approach 2 — 2024-04-14 21:58 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 40.8 MB*

```java
class Solution {
    public int reverse(int x) {
        long ans=0;
        while (x != 0){
           int temp=x%10;
            ans=(10*ans)+temp; 
            x/=10;
        }
        if(ans> Integer.MAX_VALUE || ans<Integer.MIN_VALUE){
            return 0;
        }
        if(x<0) return (int)(-1*ans);
        return (int)ans;
    }
}
```
