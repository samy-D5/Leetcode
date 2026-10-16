# 1683. Invalid Tweets

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/invalid-tweets/
**Tags:** Database

## Approach 1 — 2026-05-22 00:52 (pythondata)

*Runtime: 301 ms (faster than 40.5%) · Memory: 67.1 MB*

```pythondata
import pandas as pd

def invalid_tweets(tweets: pd.DataFrame) -> pd.DataFrame:
    invalid =tweets[tweets['content'].str.len()>15]
    return invalid[['tweet_id']]
```
