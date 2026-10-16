# 3248. Snake in Matrix

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/snake-in-matrix/
**Tags:** Array, String, Simulation

## Approach 1 — 2025-06-15 23:59 (cpp)

*Runtime: 0 ms (faster than 100.0%) · Memory: 35 MB*

```cpp
class Solution {
public:
    int finalPositionOfSnake(int girdSize, vector<string>& commands) {
        int x = 0, y = 0, n = commands.size();
        for(int i = 0; i < n; i++){
            string s = commands[i];
            if(s == "UP"){
                x--;
            }
            else if(s == "DOWN"){
                x++;
            }
            else if(s == "RIGHT"){
                y++;
            }
            else{
                y--;
            }
        }
        return (x * girdSize) + y;
    }
};
```
