# 2182. Construct String With Repeat Limit

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/construct-string-with-repeat-limit/
**Tags:** Hash Table, String, Greedy, Heap (Priority Queue), Counting

## Approach 1 — 2024-12-30 23:35 (java)

*Runtime: 18 ms (faster than 66.2%) · Memory: 45.7 MB*

```java
class Solution {
    public String repeatLimitedString(String s, int repeatLimit) {
        StringBuilder res = new StringBuilder();
        int[] alpha = new int[26];
        for(char ch: s.toCharArray()){
            alpha[ch-'a']++;
        }
        char t = 'z';
        int val = 0;
        for(int i=25; i>=0; i--){
            if(alpha[i]>0){
                while(val>0 && alpha[i]>0){
                    res.append((char)('a'+i));
                    alpha[i]--;
                    for(int j=0; j<Math.min(repeatLimit, val); j++){
                        res.append(t);
                    }
                    val = val - Math.min(repeatLimit, val);
                }
                if(alpha[i]>0){
                    for(int j=0; j<Math.min(repeatLimit, alpha[i]); j++){
                        res.append((char)('a'+i));
                    }
                    alpha[i] = alpha[i] - Math.min(repeatLimit, alpha[i]);
                }
                if(alpha[i]>0){
                    t = (char)('a'+i);
                    val = alpha[i];
                }
            }
        }
        return res.toString();
    }
}
```
