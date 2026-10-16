# 1726. Tuple with Same Product

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/tuple-with-same-product/
**Tags:** Array, Hash Table, Counting

## Approach 1 — 2025-02-22 23:00 (java)

*Runtime: 225 ms (faster than 30.4%) · Memory: 79 MB*

```java
class Solution {
    public int tupleSameProduct(int[] nums) {
        HashMap<Integer, Integer> product = new HashMap<>();
        int count=0;
        for(int i=0;i<nums.length;i++){
            for(int j=i+1;j<nums.length;j++){
                int pro= nums[i]*nums[j];
                count+= 8*product.getOrDefault(pro, 0);
                product.put(pro, product.getOrDefault(pro, 0)+1);
            }
        }
        return count;
    }
}
```
