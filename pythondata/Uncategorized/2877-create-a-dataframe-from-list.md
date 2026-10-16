# 2877. Create a DataFrame from List

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/create-a-dataframe-from-list/
**Tags:** 

## Approach 1 — 2025-06-07 12:56 (pythondata)

*Runtime: 261 ms (faster than 47.6%) · Memory: 66.2 MB*

```pythondata
import pandas as pd

def createDataframe(student_data: List[List[int]]) -> pd.DataFrame:
    col = ['student_id', 'age']
    return pd.DataFrame(student_data, columns = col)
```

## Approach 2 — 2025-06-07 12:57 (pythondata)

*Runtime: 248 ms (faster than 74.1%) · Memory: 65.5 MB*

```pythondata
import pandas as pd

def createDataframe(student_data: List[List[int]]) -> pd.DataFrame:
    return pd.DataFrame(student_data, columns = ['student_id', 'age'])
```
