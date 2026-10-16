# 2888. Reshape Data: Concatenate

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reshape-data-concatenate/
**Tags:** 

## Approach 1 — 2025-11-21 01:08 (pythondata)

*Runtime: 305 ms (faster than 46.2%) · Memory: 66.8 MB*

```pythondata
import pandas as pd

def concatenateTables(df1: pd.DataFrame, df2: pd.DataFrame) -> pd.DataFrame:
    return pd.concat([df1,df2])
```

## Approach 2 — 2026-06-01 00:54 (pythondata)

*Runtime: 290 ms (faster than 74.9%) · Memory: 66.9 MB*

```pythondata
import pandas as pd

def concatenateTables(df1: pd.DataFrame, df2: pd.DataFrame) -> pd.DataFrame:
    return pd.concat([df1,df2],axis=0)
```
