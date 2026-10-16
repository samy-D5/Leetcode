# 575. Distribute Candies

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/distribute-candies/
**Tags:** Array, Hash Table

## Approach 1 — 2025-09-24 23:11 (java)

*Runtime: 31 ms (faster than 55.9%) · Memory: 45.6 MB*

```java
class Solution {
    public int distributeCandies(int[] ct) {
        int candy = ct.length/2;
        HashSet<Integer> set = new HashSet<>();
        for(int i=0; i<ct.length; i++){
            set.add(ct[i]);
        }
        return Math.min(candy,set.size());
    }
}
```

## Approach 2 — 2025-09-24 23:19 (java)

*Runtime: 4 ms (faster than 99.9%) · Memory: 46.4 MB*

```java
class Solution {
    public int distributeCandies(int[] ct) {
        boolean[] seen = new boolean[200001];
        int offset = 100000;
        int unique = 0;
        int limit = ct.length/2;
        for(int c:ct){
            int index = c+offset;
            if(!seen[index]){
                seen[index]=true;
                unique++;
                if(unique==limit) break;
            }
        }
        return unique;
    }
}
```
