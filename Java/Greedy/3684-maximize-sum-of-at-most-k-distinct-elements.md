# 3684. Maximize Sum of At Most K Distinct Elements

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/maximize-sum-of-at-most-k-distinct-elements/
**Tags:** Array, Hash Table, Greedy, Sorting

## Approach 1 — 2026-04-11 20:38 (java)

*Runtime: 9 ms (faster than 52.2%) · Memory: 47.9 MB*

```java
class Solution {
    public int[] maxKDistinct(int[] nums, int k) {
        Set<Integer> set = new HashSet<>();
        for(int x:nums) set.add(x);

        int ans[] = new int[set.size()];
        int result[] = new int[Math.min(k, set.size())];
        int index = 0;
        for(Integer x:set){
            // if(index==ans.length) break;
            ans[index++]= x;
        }
        Arrays.sort(ans);
        index=ans.length-1;
        for(int i=0; i<result.length; i++){
            result[i]=ans[index--];
        }
        return result;
    }
}
```
