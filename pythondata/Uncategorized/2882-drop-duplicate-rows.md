# 2882. Drop Duplicate Rows

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/drop-duplicate-rows/
**Tags:** 

## Approach 1 — 2024-12-22 21:16 (pythondata)

*Runtime: 552 ms (faster than 5.2%) · Memory: 66.7 MB*

```pythondata
import pandas as pd

def dropDuplicateEmails(customers: pd.DataFrame) -> pd.DataFrame:
    return customers.drop_duplicates(subset=['email'])
```
