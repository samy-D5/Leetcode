# 3042. Count Prefix and Suffix Pairs I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-prefix-and-suffix-pairs-i/
**Tags:** Array, String, Trie, Rolling Hash, String Matching, Hash Function

## Approach 1 — 2025-01-21 11:58 (java)

*Runtime: 2 ms (faster than 100.0%) · Memory: 42.1 MB*

```java
class Solution {
    public int countPrefixSuffixPairs(String[] words) {
        int n=words.length, cnt=0;
        for(int i=0; i<n; i++){
            for(int j=i+1; j<n; j++){
                if(isPrefixAndSuffix(words[i], words[j]))
                    cnt++;
            }
        }
        return cnt;
    }
    boolean isPrefixAndSuffix(String str1, String str2){
        if (str2.startsWith(str1) && str2.endsWith(str1) )
            return true;
        return false;
    }
}
```
