# 1773. Count Items Matching a Rule

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-items-matching-a-rule/
**Tags:** Array, String

## Approach 1 — 2025-06-08 12:40 (java)

*Runtime: 6 ms (faster than 32.7%) · Memory: 50.8 MB*

```java
class Solution {
    public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int res=0;

        for(int i=0; i<items.size(); i++){
            if(ruleKey.equals("type") && items.get(i).get(0).equals(ruleValue)) res++;
            if(ruleKey.equals("color") && items.get(i).get(1).equals(ruleValue)) res++;
            if(ruleKey.equals("name") && items.get(i).get(2).equals(ruleValue)) res++;
        }
        return res;
    }
}
```

## Approach 2 — 2025-06-08 12:44 (java)

*Runtime: 3 ms (faster than 99.7%) · Memory: 51 MB*

```java
class Solution {
    public int countMatches(List<List<String>> items, String ruleKey, String ruleValue) {
        int res=0;
        int ind=0;

        if(ruleKey.equals("type")) ind=0;
        else if(ruleKey.equals("color")) ind=1;
        else if(ruleKey.equals("name")) ind=2;

        for(List<String>item: items){
            if(item.get(ind).equals(ruleValue)) res++;
        }

        return res;
    }
}
```
