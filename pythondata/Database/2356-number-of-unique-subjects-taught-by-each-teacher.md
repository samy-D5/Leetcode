# 2356. Number of Unique Subjects Taught by Each Teacher

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-unique-subjects-taught-by-each-teacher/
**Tags:** Database

## Approach 1 — 2026-06-02 08:58 (pythondata)

*Runtime: 290 ms (faster than 55.0%) · Memory: 67.8 MB*

```pythondata
import pandas as pd

def count_unique_subjects(teacher: pd.DataFrame) -> pd.DataFrame:
    result=teacher.groupby('teacher_id')['subject_id'].nunique().reset_index()
    result.rename(columns={'subject_id':'cnt'}, inplace=True)
    return result
```
