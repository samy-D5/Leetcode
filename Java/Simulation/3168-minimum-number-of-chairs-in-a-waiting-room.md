# 3168. Minimum Number of Chairs in a Waiting Room

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/minimum-number-of-chairs-in-a-waiting-room/
**Tags:** String, Simulation

## Approach 1 — 2024-08-04 22:33 (java)

*Runtime: 2 ms (faster than 4.8%) · Memory: 42.3 MB*

```java
class Solution {
    public int minimumChairs(String s) {
        while(s.contains("LE"))
            s=s.replace("LE","");
        s=s.replace("L","");
        return s.length();
    }
}
```

## Approach 2 — 2024-08-04 22:37 (java)

*Runtime: 1 ms (faster than 99.8%) · Memory: 42.1 MB*

```java
class Solution {
    public int minimumChairs(String s) {
        int res=0 , max=0;
        for(char i:s.toCharArray()){
            if(i=='E') res++;
            else{
                max=Math.max(res,max);
                res--;
            }
        }
        max=Math.max(res,max);
        return max;
    }
}
```

## Approach 3 — 2024-08-04 22:39 (java)

*Runtime: 1 ms (faster than 99.8%) · Memory: 42.6 MB*

```java
class Solution {
    public int minimumChairs(String s) {
        int res=0 , max=0;
        for(char i:s.toCharArray()){
            if(i=='E') res++;
            else  res--;
            if(res>max) max=res;
        }
        return max;
    }
}
```
