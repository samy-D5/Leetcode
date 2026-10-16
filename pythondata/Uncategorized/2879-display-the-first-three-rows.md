# 2879. Display the First Three Rows

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/display-the-first-three-rows/
**Tags:** 

## Approach 1 — 2024-08-11 23:11 (pythondata)

*Runtime: 398 ms (faster than 5.2%) · Memory: 69 MB*

```pythondata
import pandas as pd

def selectFirstRows(employees: pd.DataFrame) -> pd.DataFrame:
    return employees.head(3)
```
