# 2553. Separate the Digits in an Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/separate-the-digits-in-an-array/
**Tags:** Array, Simulation

## Approach 1 — 2026-05-11 21:56 (java)

*Runtime: 6 ms (faster than 49.2%) · Memory: 45.8 MB*

```java
class Solution {
    public int[] separateDigits(int[] nums) {
        List<Integer> list = new ArrayList<>();
        for(int x: nums){
            String s = Integer.toString(x);
            for(int i=0; i<s.length();i++){
                list.add(s.charAt(i)-'0');
            }
        }
        int[]ans=new int[list.size()];
        for(int i=0; i<list.size(); i++) ans[i]=list.get(i);
        return ans;
    }
}
```
