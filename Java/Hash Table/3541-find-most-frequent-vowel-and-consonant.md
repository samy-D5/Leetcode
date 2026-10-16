# 3541. Find Most Frequent Vowel and Consonant

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-most-frequent-vowel-and-consonant/
**Tags:** Hash Table, String, Counting

## Approach 1 — 2025-06-09 12:55 (java)

*Runtime: 1 ms (faster than 100.0%) · Memory: 42.5 MB*

```java
class Solution {
    public int maxFreqSum(String s) {
        boolean vowel[] = new boolean[26];
        for(char c: new char[]{'a', 'e', 'i', 'o', 'u'}) vowel[c - 'a']=true;

        int con[] = new int[26];
        int vow[] = new int[26];

        for(char ch: s.toCharArray()){
            int ind = ch - 'a';
            if(vowel[ind]) vow[ind]++;
            else con[ind]++;
        }

        int maxv = 0;
        int maxc = 0;

        for(int i=0; i<26; i++){
            maxv = Math.max(maxv, vow[i]);
            maxc = Math.max(maxc, con[i]);
        }

        return maxc + maxv;
    }
}
```
