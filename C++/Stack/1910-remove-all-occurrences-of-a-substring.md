# 1910. Remove All Occurrences of a Substring

**Difficulty:** Medium
**Link:** https://leetcode.com/problems/remove-all-occurrences-of-a-substring/
**Tags:** String, Stack, Simulation

## Approach 1 — 2025-06-16 00:14 (cpp)

*Runtime: 3 ms (faster than 32.2%) · Memory: 12.2 MB*

```cpp
class Solution {
public:
    string removeOccurrences(string s, string part) {
	string x = s;
	int n = s.size(), m = part.size(), i, j;
	for (i = 0, j = 0; i < n; i++) {
		x[j++] = s[i];
		if (j >= m && x.substr(j - m, m) == part)
			j -= m;
	}
	return x.substr(0, j);
}
};
```
