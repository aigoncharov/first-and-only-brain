---
{"dg-publish":true,"permalink":"/math/probability/discrete-random-variables/","created":"","updated":""}
---

#probability 

A [[Math/Probability/Random variable\|Random variable]] X is discrete** if there a finite list of values $a_1,a_{2},\dots$ or an infinite list of values $a_{1},a_{2},\dots$ such that $P(X = a_{j}) = 1$. In other words, even though the function could take any real value, there is a distinguished finite set of values that it takes with probability 1. 
See [Math StackExchange](https://math.stackexchange.com/a/3320503/1186928).

If X is discrete r.v. (random variable), then the finite or countably infinite set of values x such that $P(X=x) > 0$ is called the **support of X**.
It is a part of the sample space where $P(X) > 0$.

**Indicator random variable** of an event A is the r.v. which equals 1 if A occurs and 0 otherwise. We will denote the indicator r.v. of A by $I_{A}$ or $I(A)$. Note that $I_{A} \sim Bern(p)$ with $p=P(A)$.

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

