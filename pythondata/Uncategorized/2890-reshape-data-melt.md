# 2890. Reshape Data: Melt

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/reshape-data-melt/
**Tags:** 

## Approach 1 — 2026-05-29 00:11 (pythondata)

*Runtime: 346 ms (faster than 10.8%) · Memory: 66.9 MB*

```pythondata
import pandas as pd

def meltTable(report: pd.DataFrame) -> pd.DataFrame:
    return pd.melt(report, id_vars=['product'], var_name='quarter', value_name='sales')
```
