# 69. Sqrt(x)

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/sqrtx/
**Tags:** Math, Binary Search, Newton's Method

## Approach 1 — 2024-07-15 10:04 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 40.9 MB*

```java
class Solution {
    public int mySqrt(int x) {
        if(x == 0) return 0;
        int le=1 , ri=Integer.MAX_VALUE;
        while(true){
            int mid = le+(ri-le)/2;
            if(mid > x/mid) ri= mid-1;
            else {
                if(mid+1 > x/(mid+1)) return mid;
                le = mid+1;
            }
        }
    }
}
```
