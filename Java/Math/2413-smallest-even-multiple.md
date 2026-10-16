# 2413. Smallest Even Multiple

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/smallest-even-multiple/
**Tags:** Math, Number Theory

## Approach 1 — 2024-08-20 23:37 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.1 MB*

```java
class Solution {
        public int smallestEvenMultiple(int n) {
        return n << (n & 1);
    }
}
```

## Approach 2 — 2024-08-21 10:55 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.5 MB*

```java
class Solution {
        public int smallestEvenMultiple(int n) {
        return n%2==0?n:n*2;
    }
}
```

## Approach 3 — 2024-08-21 10:55 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.3 MB*

```java
class Solution {
        public int smallestEvenMultiple(int n) {
        return n*(n%2+1);
    }
}
```

## Approach 4 — 2024-08-21 11:18 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.8 MB*

```java
class Solution {
        public int smallestEvenMultiple(int n) {
        if(n%2==0) return n;
        else return n*2;
    }
}
```

## Approach 5 — 2024-08-21 11:20 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.3 MB*

```java
class Solution {
        public int smallestEvenMultiple(int n) {
        int i=2;
        while(true){
            if(i%n==0 && i%2==0) break;
            i++;
        }
        return i;
    }
}
```
