# 1486. XOR Operation in an Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/xor-operation-in-an-array/
**Tags:** Math, Bit Manipulation

## Approach 1 — 2024-10-04 22:09 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.1 MB*

```java
class Solution {
    public int xorOperation(int n, int start) {
        int ans=0;
        int[] num=new int[n];
        for(int i=0;i<n;i++){
            num[i] = start + 2 * i;
        }
        for(int i=0;i<num.length;i++){
            ans=ans^num[i];
        }
        return ans;
    }
}
```

## Approach 2 — 2024-10-04 22:11 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.6 MB*

```java
class Solution {
    public int xorOperation(int n, int start) {
        int ans=start;
        //int[] num=new int[n];
        for(int i=1;i<n;i++){
            ans ^= start + 2 * i;
        }
        return ans;
    }
}
```
