---
{"dg-publish":true,"permalink":"/math/probability/distributions/","created":"","updated":""}
---

#probability 
For PMF see [[Math/Probability/Discrete random variables\|Discrete random variables]]

## Poisson distribution

$$X \sim Pois(\lambda)$$
$$P(X = k) = \frac{e^{-\lambda}\lambda^{k}}{k!}$$ 
where k = 0,1,2,...

## Bernoulli distribution
$$X \sim Bern(p)$$
$P(X = 1) = p$, $P(X = 0) = 1 - p$, where p is the parameter of the distribution, 0 < p < 1. Sample space - $\{0,1\}$.

**Bernoulli trial** - experiment that result in a success of failure (1 or 0).

## Binomial distribution

$$X \sim Bin(n,p)$$
where n - number of independent Bernoulli trials, p - success probability of each trial, X - number of successes.

If $X \sim Bin(n,p)$, then $X = X_{1} + X_{2} + \dots + X_{n}$, where $X_{i}$ are i.i.d. ([[Math/Probability/Random variable\|Random variable]]) $Bern(p)$.

If $X \sim Bin(n,p)$, $Y \sim Bin(m , p)$, X and Y are independent, then $X + Y \sim Bin(n + m, p)$

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

## Discrete uniform
$$X \sim DUnif(C)$$
where C is a finite nonempty set of numbers and we choose one of them uniformly at random

### PMF
$$P(X = x) = \frac{1}{|C|}$$
for $x \in C$
