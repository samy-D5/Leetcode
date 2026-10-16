# 1741. Find Total Time Spent by Each Employee

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/find-total-time-spent-by-each-employee/
**Tags:** Database

## Approach 1 — 2026-05-20 01:02 (pythondata)

*Runtime: 325 ms (faster than 73.9%) · Memory: 67.5 MB*

```pythondata
import pandas as pd

import pandas as pd

def total_time(employees: pd.DataFrame) -> pd.DataFrame:
    employees['time_spent'] = employees['out_time'] - employees['in_time']
    result = employees.groupby(['emp_id', 'event_day'])['time_spent'].sum().reset_index()
    result.rename(columns={'event_day': 'day', 'time_spent': 'total_time'}, inplace=True)
    return result
```
