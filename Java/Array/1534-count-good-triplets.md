# 1534. Count Good Triplets

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-good-triplets/
**Tags:** Array, Enumeration

## Approach 1 — 2024-10-06 22:17 (java)

*Runtime: 13 ms (faster than 70.3%) · Memory: 40.8 MB*

```java
class Solution {
    public int countGoodTriplets(int[] arr, int a, int b, int c) {
        int n=arr.length;
        int count=0;
        for(int i=0;i<n;i++){
            for(int j=i+1;j<n;j++){
                for(int k=j+1;k<n;k++){
                    if(Math.abs(arr[i]-arr[j])<=a && Math.abs(arr[j]-arr[k])<=b && Math.abs(arr[i]-arr[k])<=c){
                            count++;
                    }
                }
            }
        }
        return count;
    }
}
```
