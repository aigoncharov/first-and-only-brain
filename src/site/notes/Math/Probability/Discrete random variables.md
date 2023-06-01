---
{"dg-publish":true,"permalink":"/math/probability/discrete-random-variables/","created":"","updated":""}
---

#probability 
**Random variable** - function mapping the sample space ([[Math/Probability/Definition of probability\|Definition of probability]]) to the real numbers.

A **random variable X is discrete** if there a finite list of values $a_1,a_{2},\dots$ or an infinite list of values $a_{1},a_{2},\dots$ such that $P(X = a_{j}) = 1$. In other words, even though the function could take any real value, there is a distinguished finite set of values that it takes with probability 1. 
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

## Poisson distribution

$$X \sim Pois(\lambda)$$
$$P(X = k) = \frac{e^{-\lambda}\lambda^{k}}{k!}$$where k = 0,1,2,...

## Bernoulli distribution
$$X \sim Bern(p)$$
$P(X = 1) = p$, $P(X = 0) = 1 - p$, where p is the parameter of the distribution, 0 < p < 1. Sample space - $\{0,1\}$.

**Bernoulli trial** - experiment that result in a success of failure (1 or 0).

## Binomial distribution

$$X \sim Bin(n,p)$$
where n - number of independent Bernoulli trials, p - success probability of each trial, X - number of successes.

### PMF
$$P(X = k) = {n \choose k}p^{k}(1-p)^{n-k}$$
## Hypergeometric
$$X \sim HGeom(w,b,n)$$
where $w$ and $b$ are numbers of different opposing outcomes, n - number of trials **without** replacement.

> Binomial with dependent trials

### Story
Consider an urn with $w$ white balls and $b$ black balls. We draw $n$ balls out of the urn at random **without** replacement, such that ${w+b} \choose n$ are equally likely. Let X be the number of white balls in the sample. Then X is said to have Hypergeometric distribution.

### PMF

$P(X=k)=\frac{{w \choose k}{b \choose {n - k}}}{{w + b} \choose n}$
for k satisfying $0 \leq k \leq w$, $0 \leq n - k \leq b$.

See Vandermonde's identity in [[Math/Probability/Sampling\|Sampling]]
