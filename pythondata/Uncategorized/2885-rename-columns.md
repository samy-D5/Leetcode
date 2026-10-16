# 2885. Rename Columns

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/rename-columns/
**Tags:** 

## Approach 1 — 2026-05-30 01:48 (pythondata)

*Runtime: 259 ms (faster than 92.3%) · Memory: 66.6 MB*

```pythondata
import pandas as pd

def renameColumns(students: pd.DataFrame) -> pd.DataFrame:
    students.rename(columns={'id': 'student_id', 'first': 'first_name', 'last': 'last_name', 'age': 'age_in_years'}, inplace=True)
    return students
```
