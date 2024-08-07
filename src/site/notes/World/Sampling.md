---
{"dg-publish":true,"permalink":"/world/sampling/"}
---

#probability 

## Multiplication rule
If A has a outcomes **and** for each of them B has b outcomes, then the compound experiment has $ab$ outcomes.

## Ordered with replacement
n objects, k choices. Choosing a certain object does not preclude it from being chosen again.
$$S = n^k$$
Example: set of n elements (A = {1,2,3}), we draw k samples from the set, order matters 
## Ordered without replacement
n objects, k choices. Choosing a certain object precludes it from being chosen again.
$$S = n(n-1)(n-2)\dots(n-k+1) = \prod_{m=0}^{k-1}(n-m) = \frac{n!}{(n-k)!}$$
## Unordered without replacement
n objects, k choices. Choosing a certain object precludes it from being chosen again. Order does not matter.
$$S = \frac{S_{ordered\:without\:replacement}}{number\:of\:ways\:to\:order\:choices} = \frac{\prod_{m=0}^{k-1}(n-m)}{k!} = \frac{n!}{(n-k)!k!}$$
Also written as $n \choose k$, also $C_{n}^{k}$

$$C_{n}^{k} = C_{n-1}^{k-1} + C_{n-1}^k$$
$$
C_{n}^{0} + C_{n}^{1} + C_{n}^{2} + \dots + C_{n}^{n} = 2^{n}
$$

## Unordered sampling with replacement
n objects, k choices. Choosing a certain object does not preclude it from being chosen again. Order does not matter.
$$S = S_{unordered\:without\:replacement}(n_{items}+ (k-1)_{separators})  =
{n + k - 1 \choose n} =
{n + k -1 \choose k -1}$$
Also written as $C_{n+k-1}^{n}$

Example 1: $x_{1} + x_{2} + \dots + x_{k} = n$, number of solutions = $C_{n+k-1}^{n}$. Imagine n balls and (k-1) separators, and then try to juggle separators to associate balls to various Xes.

Example 2: $x_{1} + x_{2} + \dots + x_{k} \leq n$, number of solutions = $C_{n+k}^{n}$. Imagine a synthetic var $x_{k+1}$ that transforms $x_{1} + x_{2} + \dots + x_{k} \leq n$ into $x_{1} + x_{2} + \dots + x_{k} + x_{k+1} = n$. It fills the difference that makes it an inequality out an equality.
## Permutation
Permutation of $1,2,3,\dots,n$ is an arrangement in some order. By sampling without replacement, with k = n, $S = n!$

## Birthday problem
There are $k$ people in a room. Assume each person's birthday is equally likely to be any of the 365 days of the year (we exclude February 29), and that people's birthdays are independent (we assume there are no twins in the room). What is the probability that two or more people in the group have the same birthday?

$$
P(no\:birthday\:match) =
\frac{permutations\:of\:365-k\:days\:when\:people\:have\:different\:birthdays}{all\:possible\:ways\:to\:choose\:k\:birthdays\:out\:of\:365\:days} =
\frac{365*364*\dots*(365-k+1)}{365^{k}} =
\frac{365!}{365^{k}*(365-k)!}
$$

$$P(match) = 1 - P(no\:birthday\:match)$$
## Vandermonde's identity
$${ m + n \choose k } = \sum\limits_{j=0}^{k} {m \choose j} {n \choose k - j}$$

## Hypergeometric probability
Say, we have a random sample $n$ out of $N$ items ($N \choose n$). Then we select a new sample $m$ out of $N$ items ($N \choose m$). The probability that **exactly** $k$ of $m$ items were in the first sample $n$ is: 

$$
\frac{{n \choose k} {N - n \choose m - k}}{{N \choose m}}
$$

## Inclusion-exclusion theorem

$$
P(\bigcup\limits_{i=1}^{n}A_{i}) =
\sum\limits_{i}^{n}P(A_{i}) -
\sum\limits_{j=i+1}^{n}P(A_{i} \cap A{j}) +
\sum\limits_{k=j+1}^{n}P(A_{i} \cap A{j} \cap A_{k}) -
\dots +
(-1)^{n+1}P(A_1 \cap\dots \cap A_n)
$$
Famous application: de Montmort's matching problem