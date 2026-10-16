# 2886. Change Data Type

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/change-data-type/
**Tags:** 

## Approach 1 — 2026-05-10 23:13 (pythondata)

*Runtime: 271 ms (faster than 76.3%) · Memory: 67.1 MB*

```pythondata
import pandas as pd

def changeDatatype(students: pd.DataFrame) -> pd.DataFrame:
    df= pd.DataFrame(students)
    df["grade"]=df[["grade"]].astype(int)
    return df
```

## Approach 2 — 2026-05-10 23:14 (pythondata)

*Runtime: 269 ms (faster than 79.4%) · Memory: 66.1 MB*

```pythondata
import pandas as pd

def changeDatatype(students: pd.DataFrame) -> pd.DataFrame:
    students["grade"]=students["grade"].astype(int)
    return students
```
