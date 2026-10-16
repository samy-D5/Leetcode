# 2356. Number of Unique Subjects Taught by Each Teacher

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-unique-subjects-taught-by-each-teacher/
**Tags:** Database

## Approach 1 — 2024-08-19 00:12 (mysql)

*Runtime: 453 ms (faster than 99.6%) · Memory: 0B*

```mysql
# Write your MySQL query statement below
Select  teacher_id ,
count(distinct subject_id ) as cnt from Teacher
group by teacher_id
```

## Approach 2 — 2025-11-22 00:14 (mysql)

*Runtime: 465 ms (faster than 98.4%) · Memory: 0B*

```mysql
Select  teacher_id ,
count(distinct subject_id ) as cnt from Teacher
group by teacher_id
```
