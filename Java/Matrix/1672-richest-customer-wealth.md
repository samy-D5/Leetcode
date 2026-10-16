# 1672. Richest Customer Wealth

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/richest-customer-wealth/
**Tags:** Array, Matrix

## Approach 1 — 2024-06-18 23:31 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43 MB*

```java
class Solution {
    public int maximumWealth(int[][] accounts) {
        int []sum=new int[accounts.length];
        int s,max=0;
        for(int i=0;i<accounts.length;i++){
            s=0;
            for(int j=0;j<accounts[i].length;j++){
                s+=accounts[i][j];
            }
            sum[i]=s;
        }
        for(int i=0;i<sum.length;i++){
            if(sum[i]>max)  max=sum[i];
        }
        return max;
    }
}
```
