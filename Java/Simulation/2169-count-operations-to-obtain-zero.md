# 2169. Count Operations to Obtain Zero

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-operations-to-obtain-zero/
**Tags:** Math, Simulation

## Approach 1 — 2024-06-27 10:54 (java)

*Runtime: 1 ms (faster than 88.9%) · Memory: 40 MB*

```java
class Solution {
    public int countOperations(int num1, int num2) {
        int count=0;
        while(num1!=0 && num2!=0){
            if(num1 >= num2){
                num1=num1-num2;
                count++;
            }
            else{
                num2=num2-num1;
                count++;
            }
        }
        return count;
    }
}
```
