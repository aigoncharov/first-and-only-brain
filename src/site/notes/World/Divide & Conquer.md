---
{"dg-publish":true,"permalink":"/world/divide-and-conquer/"}
---

#algorithms 
## Median of medians
Find k-th smallest element:
```
FastSelect(A, k):
	1. Break A into n/5 groups: G_1, G_2, ... G_{n/5} // O(n)
	2. for i = 1 -> n/5: sort G_i, let m_i = median of G_i
	3. S = {m_1, m_2, ..., m_{n/5}}
	4. p = FastSelect(S, n/10) // T(n/5)
	5. Partition A into A<p, A=p, A>p
	6. if k < |A<p|, then return FastSelect(A<p, k) // T(3n/4)
	7. if k < |A<p|+|A=p|, then return p
	8. return FastSelect(A>p, k- |A<p| - |A=p|)
```
**Runtime:** T(n) = O(n) + T(n/5) + T(3n/4) = O(n)
## Solving recurrences
$T(n) = aT(n/b) + O(n)$, where a>0, b>1

$T(n) = cn(1 + a/b + (a/b)^2 + ... + (a/b)^{log_b{n-1}}) + a^{log_b{n}}T(1)$

$T(n) = O(n^{log_b{a}})$, if a > b
$T(n) = O(n log{n})$, if a=b
$T(n) = O(n)$, if a < b