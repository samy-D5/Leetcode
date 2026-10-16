# 3184. Count Pairs That Form a Complete Day I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-pairs-that-form-a-complete-day-i/
**Tags:** Array, Hash Table, Counting

## Approach 1 — 2024-06-16 08:25 (java)

*Runtime: 1 ms (faster than 99.5%) · Memory: 42.3 MB*

```java
class Solution {
    public int countCompleteDayPairs(int[] hours) {
        int count=0;
        int days=24;
        for(int i=0;i<hours.length-1;i++){
            for(int j=i+1;j<hours.length;j++){
                if((hours[i]+hours[j])%days==0){
                  
                    count++;
                }
            }
        }
        return count;
    }
}
```
