# 2469. Convert the Temperature

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/convert-the-temperature/
**Tags:** Math

## Approach 1 — 2024-01-26 11:33 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 42 MB*

```java
class Solution {
    public double[] convertTemperature(double celsius) {
         double kelvin= celsius+273.15;
         double farenheit= celsius*1.80+32.00;
         double []ans={kelvin,farenheit};
         return ans;
    }
}
```

## Approach 2 — 2024-06-04 22:32 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 41.8 MB*

```java
class Solution {
    public double[] convertTemperature(double celsius) {
         return new double[] {celsius+273.15,(celsius*1.8)+32};
    }
}
```
