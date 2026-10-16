# 2429. Minimize XOR

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/minimize-xor/
**Tags:** Greedy, Bit Manipulation

## Approach 1 — 2025-01-23 10:25 (java)

*Runtime: 1 ms (faster than 31.1%) · Memory: 41.2 MB*

```java
class Solution {
        public int minimizeXor(int num1, int num2) {
        int a = Integer.bitCount(num1), b = Integer.bitCount(num2), res = num1;
        for (int i = 0;i <32;++i) {
            if(a>b && ((1<<i) & num1) >0) {
                res ^= 1<<i;
                a--;
            }
            if(a<b && ((1<<i) & num1)==0) {
                res ^= 1<<i;
                a++;
            }
        }
        return res;
    }
}
```
