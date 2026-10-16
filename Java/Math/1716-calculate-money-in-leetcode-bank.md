# 1716. Calculate Money in Leetcode Bank

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/calculate-money-in-leetcode-bank/
**Tags:** Math

## Approach 1 — 2024-01-29 13:17 (java)

*Runtime: 1 ms (faster than 69.5%) · Memory: 40.2 MB*

```java
class Solution {
    public int totalMoney(int n) {
        int ans=0;
        int mon=1;
        int x=1;
        for(int i=0;i<n;i++){
            if(i%7==0&&i!=0){
                mon++;
                x=mon;
            }
            ans+=x;
            x++;
        }
        return ans;
    }
}
```
