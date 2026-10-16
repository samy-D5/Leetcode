# 1795. Rearrange Products Table

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/rearrange-products-table/
**Tags:** Database

## Approach 1 — 2026-05-17 23:49 (pythondata)

*Runtime: 333 ms (faster than 46.0%) · Memory: 67.3 MB*

```pythondata
import pandas as pd

def rearrange_products_table(products: pd.DataFrame) -> pd.DataFrame:
    return pd.melt(
        products, id_vars='product_id', var_name='store', value_name='price'
    ).dropna()
```
