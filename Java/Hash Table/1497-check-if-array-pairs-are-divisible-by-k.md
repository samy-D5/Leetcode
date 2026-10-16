# 1497. Check If Array Pairs Are Divisible by k

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/check-if-array-pairs-are-divisible-by-k/
**Tags:** Array, Hash Table, Counting

## Approach 1 — 2024-12-14 00:14 (java)

*Runtime: 5 ms (faster than 72.4%) · Memory: 56.8 MB*

```java
class Solution {
    public boolean canArrange(int[] arr, int k) {
        int[] frequency = new int[k];
        for(int num :arr){
            num %= k;
            if(num <0) num += k;
            frequency[num]++;
        }
        if(frequency[0]%2 != 0) return false;
        for(int i = 1; i <= k/2; i++)
            if(frequency[i] != frequency[k-i]) return false;
        return true;
    }
}
```
