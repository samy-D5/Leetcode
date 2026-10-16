# 1587. Bank Account Summary II

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/bank-account-summary-ii/
**Tags:** Database

## Approach 1 — 2026-05-23 00:28 (pythondata)

*Runtime: 326 ms (faster than 74.5%) · Memory: 68.3 MB*

```pythondata
import pandas as pd

def account_summary(users: pd.DataFrame, transactions: pd.DataFrame) -> pd.DataFrame:
    
    df = (transactions.groupby('account')['amount'].sum()
                      .reset_index(name  = 'balance'))

    return df[df.balance > 10_000].merge(users).iloc[:,[2,1]]
```
