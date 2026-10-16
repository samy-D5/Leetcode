# 1693. Daily Leads and Partners

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/daily-leads-and-partners/
**Tags:** Database

## Approach 1 — 2026-06-06 00:02 (pythondata)

*Runtime: 331 ms (faster than 88.6%) · Memory: 67.6 MB*

```pythondata
import pandas as pd

def daily_leads_and_partners(daily_sales: pd.DataFrame) -> pd.DataFrame:

    return (daily_sales.groupby(['date_id', 'make_name'])
                       .nunique().reset_index()
                       .rename(columns = {'lead_id':'unique_leads',
                                         'partner_id': 'unique_partners'}))
```
