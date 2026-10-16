# 1550. Three Consecutive Odds

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/three-consecutive-odds/
**Tags:** Array

## Approach 1 — 2024-07-08 12:30 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.4 MB*

```java
class Solution {
    public boolean threeConsecutiveOdds(int[] arr) {
        for(int i=2;i<arr.length;i++){
            if(arr[i]%2!=0 && arr[i-1]%2!=0){
                if(arr[i-2]%2!=0) return true;
            }
        }
        return false;
    }
}
```
