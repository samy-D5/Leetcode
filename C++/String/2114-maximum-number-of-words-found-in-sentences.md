# 2114. Maximum Number of Words Found in Sentences

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximum-number-of-words-found-in-sentences/
**Tags:** Array, String

## Approach 1 — 2025-06-15 23:54 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 12.8 MB*

```cpp
class Solution {
public:
    int mostWordsFound(vector<string>& sentences) {
        int n=sentences.size();
        int counter, ans=0;
        for(int i=0;i<n;i++)
        {
            int k=sentences[i].length();
            counter=1;
            for(int j=0;j<k;j++)
            {
                if(sentences[i][j]==' ')
                {
                    counter++;
                }
            }
            ans=max(counter, ans);
        }
        return ans;
    }
};
```
