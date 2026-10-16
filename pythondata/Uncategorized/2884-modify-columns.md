# 2884. Modify Columns

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/modify-columns/
**Tags:** 

## Approach 1 — 2024-08-11 23:17 (pythondata)

*Runtime: 319 ms (faster than 8.0%) · Memory: 69.2 MB*

```pythondata
import pandas as pd

def modifySalaryColumn(employees: pd.DataFrame) -> pd.DataFrame:
    return employees.assign(salary=2*employees['salary'])
```

## Approach 2 — 2024-08-11 23:18 (pythondata)

*Runtime: 379 ms (faster than 5.1%) · Memory: 69.5 MB*

```pythondata
import pandas as pd

def modifySalaryColumn(employees: pd.DataFrame) -> pd.DataFrame:
    employees.salary*=2
    return employees
```
