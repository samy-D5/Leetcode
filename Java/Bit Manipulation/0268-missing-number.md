# 268. Missing Number

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/missing-number/
**Tags:** Array, Hash Table, Math, Binary Search, Bit Manipulation, Sorting

## Approach 1 — 2024-09-29 13:53 (java)

*Runtime: 5 ms (faster than 21.1%) · Memory: 45.1 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n=nums.length;
        Arrays.sort(nums);
        int freq[] = new int[n+1];
        for(int i=0;i<n;i++){
            freq[nums[i]]++;
        }
        for(int i=0;i<=n;i++){
            if(freq[i]==0){
                return i;
            }
        }
        return -1;
    }
}
```

## Approach 2 — 2024-09-29 14:00 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45.2 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n=nums.length;
        int sum=(n*(n+1))/2;
        int actual=0;
        for(int i=0;i<n;i++){
            actual+=nums[i];
        }
        return sum-actual;

    }
}
```

## Approach 3 — 2024-09-29 14:03 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 44.8 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n=nums.length;
        int sum=(n*(n+1))/2;
        //n=5 ; sum=15;
        int actual=0;
        for(int i=0;i<n;i++){
            actual+=nums[i];
        }// 1 2 4 5
        // actual=12
        return sum-actual; //15-12=3;
    }
}
```

## Approach 4 — 2024-09-29 14:07 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45.1 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n=nums.length;
        int xor1=0;
        int xor2=0;
        for(int i=0;i<n;i++){
            xor1^=nums[i];
            xor2^=(i+1);
        }
        return xor1^xor2;
    }
}
```

## Approach 5 — 2024-09-29 14:10 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 45.2 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        int n=nums.length;
        int xor1=0;
        int xor2=0;
        for(int i=0;i<n;i++){
            //1 2 4 5 , n=5
            xor1^=nums[i];// (1^2^4^5)
            xor2^=(i+1);//(1^2^3^4^5)
        }
        return xor1^xor2;//(1^2^3^4^5) ^ (1^2^4^5)
			            //= (1^1)^(2^2)^(3)^(4^4)^(5^5)
			            //= 0^0^3^0^0 
                        //= 0^3
                        //= 3.
    }
}
```

## Approach 6 — 2024-12-20 12:43 (java)

*Runtime: 5 ms (faster than 21.1%) · Memory: 45.7 MB*

```java
class Solution {
    public int missingNumber(int[] nums) {
        Arrays.sort(nums);
        int left=0, right=nums.length, mid=(left+right)/2;
        while(left<right){
            mid=(left+right)/2;
            if(nums[mid]>mid) right=mid;
            else left = mid+1;
        }
        return left;
    }
}
```
