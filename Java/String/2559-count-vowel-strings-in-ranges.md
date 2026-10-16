# 2559. Count Vowel Strings in Ranges

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/count-vowel-strings-in-ranges/
**Tags:** Array, String, Prefix Sum

## Approach 1 — 2025-01-21 11:45 (java)

*Runtime: 9 ms (faster than 30.8%) · Memory: 85.7 MB*

```java
class Solution {
    public int[] vowelStrings(String[] words, int[][] queries) {
        int n = words.length;
        int[] Prefix = new int[n + 1];
        Set<Character> vowels = new HashSet<>(Arrays.asList('a', 'e', 'i', 'o', 'u'));
        for (int i = 0; i < n; i++) {
            Prefix[i + 1] = Prefix[i];
            if (vowels.contains(words[i].charAt(0)) && vowels.contains(words[i].charAt(words[i].length() - 1)))
                Prefix[i + 1]++;
        }
        int[] ANS = new int[queries.length];
        for (int i = 0; i < queries.length; i++)
            ANS[i] = Prefix[queries[i][1] + 1] - Prefix[queries[i][0]];
        return ANS;
    }
}
```
