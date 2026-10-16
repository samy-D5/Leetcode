# 511. Game Play Analysis I

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/game-play-analysis-i/
**Tags:** Database

## Approach 1 — 2026-05-19 00:45 (pythondata)

*Runtime: 301 ms (faster than 50.4%) · Memory: 68.4 MB*

```pythondata
import pandas as pd

def game_analysis(activity: pd.DataFrame) -> pd.DataFrame:
    return activity.groupby(
        'player_id'
    ).agg(
        first_login=('event_date', 'min')
    ).reset_index()
```
