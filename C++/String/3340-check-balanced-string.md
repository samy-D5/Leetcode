# 3340. Check Balanced String

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-balanced-string/
**Tags:** String

## Approach 1 — 2025-06-16 00:05 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 8.5 MB*

```cpp
class Solution {
public:
    bool isBalanced(std::string num) {
        int evenSum = 0;
        int oddSum = 0;

        for (size_t i = 0; i < num.length(); ++i) {
            int digit = num[i] - '0';
            if (i % 2 == 0) {
                evenSum += digit;} else {
                oddSum += digit;}
        }

        return evenSum == oddSum;}
};
```
