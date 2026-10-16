# 2011. Final Value of Variable After Performing Operations

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/final-value-of-variable-after-performing-operations/
**Tags:** Array, String, Simulation

## Approach 1 — 2024-08-16 20:23 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 43.3 MB*

```java
class Solution {
    public int finalValueAfterOperations(String[] operations) {
        int ans=0;
        for(int i=0;i<operations.length;i++){
            if(operations[i].charAt(1)=='-') ans-=1;
            else ans+=1;
        }
        return ans;
    }
}
```

## Approach 2 — 2024-08-16 20:26 (java)

*Runtime: 1 ms (faster than 76.2%) · Memory: 42.5 MB*

```java
class Solution {
    public int finalValueAfterOperations(String[] operations) {
        int ans=0;
        for(int i=0;i<operations.length;i++){
            String str=operations[i];
            if(str.equals("--X") || str.equals("X--")) ans-=1;
            else ans+=1;
        }
        return ans;
    }
}
```
