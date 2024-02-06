---
{"dg-publish":true,"permalink":"/world/dynamic-programming/","created":"","updated":""}
---

#algorithms
## Longest increasing subsequence

```
for i = 1 -> n:
    L(i) = 1
    for (j = 1 -> i -1):
        if a(j) < a(i) && L(i) < L(j) + 1:
            L(i) = L(j) + 1
max = 1
for i = 1 -> n:
    if max < L(i):
        max = L(i)

return max
```
### Runtime: 
O(n^2)

## Longest common subsequence

```
for i = 1 -> n:
    L(i, 0) = 0

for j = 1 -> n:
    L(0, j) = 0

for i = 1 -> n:
    for j = 1 -> n:
        if X(i) == Y(i):
		    L(i, j) = 1 + L(i - 1, j - 1)
		else:
			L(i, j) = max(L(i - 1, j), L(i, j - 1))

return L(n, n)
```
### Runtime:
O(n^2)
## Knapsack (no repeat)

```
for b = 0 -> B: 
	K(0, b) = 0

for i = 1 -> n:
	K(i, 0) = 0

for i = 1 -> n:
	for b = 1 -> B:
		if w(i) <= b:
			K(i, b) = max{v(i) + K(i - 1, b - w(i)), K(i - 1, b)}
		else:
			K(i, b) = K(i -1, b)

return K(n, B)
```
### Runtime
O(nB) - **pseudo-polynomial**! See https://cs.stackexchange.com/a/51566
## Knapsack (repeat)

```
for b = 0 -> B:
	K(b) = 0

for i = 1 -> n:
	if w(i) < b && K(b) < v(i) + K(b - w(i)):
		K(b) = v(i) + K(b - w(i))

return K(B)
```
### Runtime:
O(nB)