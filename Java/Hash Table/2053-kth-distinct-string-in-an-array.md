# 2053. Kth Distinct String in an Array

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/kth-distinct-string-in-an-array/
**Tags:** Array, Hash Table, String, Counting

## Approach 1 — 2024-08-05 23:02 (java)

*Runtime: 70 ms (faster than 11.1%) · Memory: 43.7 MB*

```java

class Solution {
    public String kthDistinct(String[] arr, int k) {
        int distinctCount = 0;
        for (int i = 0; i < arr.length; i++) {
            if (isDistinct(arr, i)) {
                distinctCount++;
                if (distinctCount == k) {
                    return arr[i];
                }
            }
        }
        return "";
    }

    private boolean isDistinct(String[] arr, int index) {
        for (int i = 0; i < arr.length; i++) {
            if (i != index && arr[i].equals(arr[index])) {
                return false;
            }
        }
        return true;
    }
}
```
