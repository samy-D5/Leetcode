# 2798. Number of Employees Who Met the Target

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-employees-who-met-the-target/
**Tags:** Array

## Approach 1 — 2024-06-06 20:30 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42.1 MB*

```java
class Solution {
    public int numberOfEmployeesWhoMetTarget(int[] hours, int target) {
        int count=0;
        for(int i=0;i<hours.length;i++){
            if(hours[i]>=target) count++;
        }
        return count;
    }
}
```
