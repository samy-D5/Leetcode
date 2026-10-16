# 1528. Shuffle String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/shuffle-string/
**Tags:** Array, String

## Approach 1 — 2024-03-30 11:02 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.5 MB*

```java
class Solution {
    public String restoreString(String s, int[] indices) {
       char[]r=new char[indices.length];
        for(int i=0;i<indices.length;i++){
            r[indices[i]]=s.charAt(i);
        }
        return new String(r);
    }
}
```

## Approach 2 — 2024-08-31 00:29 (java)

*Runtime: 1 ms (faster than 61.1%) · Memory: 44.5 MB*

```java
class Solution{
        public String restoreString(String s,int[] indices){
                String[]shuffle=new String[indices.length];
                        StringBuilder ans=new StringBuilder();
                                for(int i=0;i<indices.length;i++)shuffle[indices[i]]=String.valueOf(s.charAt(i));
                                        for(String str:shuffle)ans.append(str);
                                                return ans.toString();
                                                    }
                                                    }
```
