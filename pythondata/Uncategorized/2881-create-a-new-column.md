# 2881. Create a New Column

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/create-a-new-column/
**Tags:** 

## Approach 1 — 2024-08-14 12:08 (pythondata)

*Runtime: 362 ms (faster than 5.0%) · Memory: 68.5 MB*

```pythondata
import pandas as pd

def createBonusColumn(employees: pd.DataFrame) -> pd.DataFrame:
    employees['bonus'] = employees['salary']*2
    return employees
```
