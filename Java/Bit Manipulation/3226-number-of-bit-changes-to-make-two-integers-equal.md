# 3226. Number of Bit Changes to Make Two Integers Equal

**Difficulty:** Easy
**Link:** https://leetcode.com/problems/number-of-bit-changes-to-make-two-integers-equal/
**Tags:** Bit Manipulation

## Approach 1 — 2024-07-21 08:52 (java)

*Runtime: 0 ms (faster than 100.0%) · Memory: 40.8 MB*

```java
class Solution {
    public int minChanges(int n, int k) {
        if (Integer.bitCount(k) > Integer.bitCount(n)) {
            return -1;
        }

        int changes = 0;

        while (n > 0 || k > 0) {
            // Compare the least significant bits of n and k
            int nBit = n & 1;
            int kBit = k & 1;

            // If nBit is 1 and kBit is 0, we need to change this bit
            if (nBit == 1 && kBit == 0) {
                changes++;
            }

            // If nBit is 0 and kBit is 1, it's impossible to make n equal to k
            if (nBit == 0 && kBit == 1) {
                return -1;
            }

            // Shift n and k to the right by 1 bit to compare the next bits
            n >>= 1;
            k >>= 1;
        }

        return changes;
    }
}
```

## Approach 2 — 2024-07-21 08:56 (java)

*Runtime: 2 ms (faster than 12.7%) · Memory: 40.7 MB*

```java
class Solution {
    public int minChanges(int n, int k) {
        int count=-1;
        String bin1 = Integer.toBinaryString(n);
        String bin2 = Integer.toBinaryString(k);
        if(bin1.equals(bin2)) return 0;
        while (bin1.length() < bin2.length()) bin1 = "0" + bin1;
        while (bin2.length() < bin1.length()) bin2 = "0" + bin2;
        count=0;
        for(int i=0;i<bin1.length();i++){
            if (bin1.charAt(i) == '1' && bin2.charAt(i) == '0') {
                count++;
            } else if (bin1.charAt(i) == '0' && bin2.charAt(i) == '1') {
                return -1; // Impossible to change 0 to 1
            }
        }
    return count;
    }
}
```
