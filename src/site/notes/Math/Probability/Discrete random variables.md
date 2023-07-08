---
{"dg-publish":true,"permalink":"/math/probability/discrete-random-variables/","created":"","updated":""}
---

#probability 

A [[Math/Probability/Random variable\|Random variable]] X is discrete** if there a finite list of values $a_1,a_{2},\dots$ or an infinite list of values $a_{1},a_{2},\dots$ such that $P(X = a_{j}) = 1$. In other words, even though the function could take any real value, there is a distinguished finite set of values that it takes with probability 1. 
See [Math StackExchange](https://math.stackexchange.com/a/3320503/1186928).

If X is discrete r.v. (random variable), then the finite or countably infinite set of values x such that $P(X=x) > 0$ is called the **support of X**.
It is a part of the sample space where $P(X) > 0$.

## Probability mass function (PMF)

The probability mass function of a discrete r.v. X is the function given by $p_{X}(x) = P(X = x)$. Note that this is positive if x is in the support of X, and 0 otherwise.

### Validity criteria
Let X be the discrete r.v. with support $x_{1}, x_{2}, \dots$. The PMF $p_{X}$ of X must satisfy:
1. Nonnegative: $p_{X}(x)>0$ if x is in the support, $p_{X}(x) = 0$ otherwise.
2. Sums to 1: $\sum\limits_{j=1}^{\infty} p_{X}(x_{j})= 1$

## Cumulative distribution function (CDF)
The cumulative distribution function (CDF) of an r.v. X is the function $F_{X}(x) = P(X \leq x)$.
Could be calculated as the sum of PMF up to x.

### Validity criteria
1. Increasing: if $x_{1} \leq x_{2}$, then $F(x_{1}) \leq f(x_{2})$
2. Right-continuous: continuous except for the possibility of having some jumps, $F(a) = \lim_{x \to a^{+} F(x)}$
3. Convergence to 0 and 1 in the limits: $\lim_{x \to -\infty} F(x) = 0$ and $\lim_{x \to \infty} F(x) = 1$

## Indicator random variable
**Indicator random variable** of an event A is the r.v. which equals 1 if A occurs and 0 otherwise. We will denote the indicator r.v. of A by $I_{A}$ or $I(A)$. Note that $I_{A} \sim Bern(p)$ with $p=P(A)$.

$$P(A) = E(I_{A})$$
### Example
A permutation $a_{1}, a_{2}, \dots, a_{n}$ of $1, 2, \dots, n$ has a _local maximum_ at $a_{j}$ if $a_{j} > a_{j-1}$ and $a_{j} > a_{j+1}$. For $n \geq 2$, what is the average number of local maxima of a random permutation of $1, 2, \dots, n$, with all $n!$ permutations equally likely?

**Solution**:
Let $I_{1}, \dots, I_{n}$ be indicator r.v.s, where $I_{j}$ is 1 if there is a local maximum at position j, and 0 otherwise. We are interested in the expected value of their sum. For $1 < j < n$, $E(I_{j}) = \frac{1}{3}$ since having a local maximum at j is equivalent to $a_{j}$ being the largest of $a_{j-1}, a_{j}, a_{j+1}$, which has probability 1/3 since all orders are equally likely. For j=1 or j=2, we have 1/2 since then there is only one neighbor. Thus, by linearity,
$$E\left(\sum\limits_{j=1}^{n}I_{j}\right)= 2\frac{1}{2} + (n-2)\frac{1}{3} = \frac{n+1}{3}$$
We account for all permutations when we consider permutations of a within a single I.