---
{"dg-publish":true,"permalink":"/math/probability/sampling/","created":"","updated":""}
---

#probability

Follows from [[Math/Probability/Multiplication rule\|Multiplication rule]]

**Ordered with replacement**: n objects, k choices. Choosing a certain object does not preclude it from being chosen again.
$$S = n^k$$
**Ordered without replacement**: n objects, k choices. Choosing a certain object precluded it from being chosen again.
$$S = n(n-1)(n-2)\dots(n-k+1) = \frac{n!}{(n-k)!}$$
**Unordered sampling without replacement:** n objects, k choices. Choosing a certain object precluded it from being chosen again. Order does not matter.
$$S = \frac{S_{ordered\:without\:replacement}}{number\:of\:ways\:to\:order\:choices} = \frac{n!}{(n-k)!k!}$$
Also written as $n \choose k$

**Unordered sampling with replacement:** n objects, k choices. Choosing a certain object does not preclude it from being chosen again. Order does not matter.
$$S = S_{unordered\:without\:replacement}(n_{items}+ (k-1)_{separators})  =
{n + k - 1 \choose n} =
{n + k -1 \choose k -1}$$

**Permutation** of $1,2,3,\dots,n$ is an arrangement in some orfder. By sampling without replacement, with k = n, $$S = n!$$
**Birthday problem**
There are $k$ people in a room. Assume each person's birthday is equally likely to be any of the 365 days of the year (we exclude February 29), and that people's birthdays are independent (we assume there are no twins in the room). What is the probability that two or more people in the group have the same birthday?

$$
P(no\:birthday\:match) =
\frac{permutations\:of\:365-k\:days\:when\:people\:have\:different\:birthdays}{all\:possible\:ways\:to\:choose\:k\:birthdays\:out\:of\:365\:days} =
\frac{365*364*\dots*(365-k+1)}{365^{k}} =
\frac{365!}{365^{k}*(365-k)!}
$$

$$P(match) = 1 - P(no\:birthday\:match)$$
