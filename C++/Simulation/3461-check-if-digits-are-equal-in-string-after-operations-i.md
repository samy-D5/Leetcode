# 3461. Check If Digits Are Equal in String After Operations I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/check-if-digits-are-equal-in-string-after-operations-i/
**Tags:** Math, String, Simulation, Combinatorics, Number Theory

## Approach 1 — 2025-06-16 00:16 (cpp)

*Runtime: 28 ms (faster than 16.0%) · Memory: 11.4 MB*

```cpp
class Solution {
public:
    bool hasSameDigits(std::string s) {
        while (s.length() > 2) {
            std::string newbornString;
            for (size_t i = 0; i < s.length() - 1; i++) {
                int firstDigit = s[i] - '0';               // Convert char to int
                int secondDigit = s[i + 1] - '0';          // Convert char to int
                int newDigit = (firstDigit + secondDigit) % 10; // Calculate new digit
                newbornString += std::to_string(newDigit); // Append new digit to the new string
            }
            s = newbornString;                             // Update s to the new string
        }
        // Check if the final two digits are the same
        return s[0] == s[1];
    }
};
```
