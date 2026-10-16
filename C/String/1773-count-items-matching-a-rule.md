# 1773. Count Items Matching a Rule

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/count-items-matching-a-rule/
**Tags:** Array, String

## Approach 1 — 2025-06-08 13:14 (c)

*Runtime: 0 ms (faster than 100.0%) · Memory: 17.4 MB*

```c
#include <string.h> //strcmp()
#define TYPE 0
#define COLOR 1
#define NAME 2

int countMatches(char*** items, int itemsSize, int* itemsColSize, char* ruleKey, char* ruleValue) {
   int match= 0;
   int c;

   switch(ruleKey[0]){
    case 't': c= TYPE; break;
    case 'c': c= COLOR; break;
    case 'n': c= NAME; break;
    default: return -1;
   }

   for(int i=0; i<itemsSize; i++){
    if(strcmp(items[i][c], ruleValue) == 0) match++;
   }

   return match;
}
```
