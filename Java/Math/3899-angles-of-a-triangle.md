# 3899. Angles of a Triangle

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/angles-of-a-triangle/
**Tags:** Array, Math, Geometry

## Approach 1 — 2026-04-12 08:41 (java)

*Runtime: 3 ms (faster than 94.1%) · Memory: 49.4 MB*

```java
class Solution {
    public double[] internalAngles(int[] sides) {
        double a = sides[0];
        double b = sides[1];
        double c = sides[2];
        if(a+b>c && b+c>a && c+a>b){
            double ans[] = new double[sides.length];
            ans[0]=Math.toDegrees(Math.acos((b*b+c*c-a*a)/(2*b*c)));
            ans[1]=Math.toDegrees(Math.acos((a*a+c*c-b*b)/(2*a*c)));
            ans[2]=Math.toDegrees(Math.acos((b*b+a*a-c*c)/(2*b*a)));
            Arrays.sort(ans);
            return ans;
        }
        return new double[0];
    }
}
```
