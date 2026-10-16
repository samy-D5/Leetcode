# 2864. Maximum Odd Binary Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-odd-binary-number/
**Tags:** Math, String, Greedy

## Approach 1 — 2024-03-30 13:16 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 43 MB*

```java
class Solution {
    public String maximumOddBinaryNumber(String s) {
        char p[]=new char[s.length()];
        int count=0;
        for(int i=0;i<s.length();i++){
            if(s.charAt(i)=='1') count++;
        }

            if(count>0) p[p.length-1]='1';
            else p[p.length-1]='0';
            count --;

        for(int i=0;i<p.length-1;i++){
            if(count>0) p[i]='1';
            else p[i]='0';
            count--;
        }
        return new String(p);
    }
}
```
