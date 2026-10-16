# 1431. Kids With the Greatest Number of Candies

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/kids-with-the-greatest-number-of-candies/
**Tags:** Array

## Approach 1 — 2024-06-06 21:02 (java)

*Runtime: 1 ms (faster than 95.3%) · Memory: 42.1 MB*

```java
class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
      int maxCandies = 0;
        for (int candy : candies) 
            maxCandies = Math.max(maxCandies, candy);
        
        List<Boolean> ans=new ArrayList<>();

        for(int candy: candies){
            if(candy+extraCandies>=maxCandies)
                ans.add(true);
            else 
                ans.add(false);
        }
        return ans;
    }
}
```

## Approach 2 — 2024-06-06 21:06 (java)

*Runtime: 1 ms (faster than 95.3%) · Memory: 42 MB*

```java
class Solution {
    public List<Boolean> kidsWithCandies(int[] candies, int extraCandies) {
      int maxCandies = candies[0];
        for (int candy : candies) {
            if(candy>maxCandies) maxCandies=candy;
        }
        List<Boolean> ans=new ArrayList<>();

        for(int candy: candies){
            if(candy+extraCandies>=maxCandies)
                ans.add(true);
            else 
                ans.add(false);
        }
        return ans;
    }
}
```
