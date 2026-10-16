# 2485. Find the Pivot Integer

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-the-pivot-integer/
**Tags:** Math, Prefix Sum

## Approach 1 — 2024-06-07 22:57 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.4 MB*

```java
class Solution {
    public int pivotInteger(int n) {
        int leftBound = 1, rightBound = n;
        int fullSum = (n * (n + 1)) / 2;
        while (leftBound <= rightBound) {
            int midNum = leftBound + (rightBound - leftBound) / 2;
            int firstHlfSum = (midNum * (midNum + 1)) / 2;
            int secondHlfSum = fullSum - firstHlfSum + midNum;
            if (firstHlfSum == secondHlfSum)
                return midNum;
            else if (firstHlfSum < secondHlfSum)
                leftBound = midNum + 1;
            else
                rightBound = midNum - 1;
        }
        return -1;
    }
}
```
