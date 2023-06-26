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

## Continuous uniform
$$X \sim Unif(a, b)$$
Uniform distribution on the interval $(a,b)$

**Standard uniform** is $Unif(0, 1)$

### PDF

$$
\begin{equation}
f(x) =
\begin{cases} \\
\frac{1}{b-a} & \text{if a < x < b} \\
0 & \text{otherwise}
\end{cases}       
\end{equation}
$$
### CDF
$$
\begin{equation}
F(x) =
\begin{cases} \\
0 & x \leq a \\
\frac{x-a}{b-a} & a < x < b \\
1 & x \geq b
\end{cases}       
\end{equation}
$$
It **follows** that $P(U \leq u) = u$ where $u \in (0,1)$.

### Location-scale transformation
Let X be an r.v. and $Y = \sigma X + \mu$, where $\sigma$ and $\mu$ are constants with $\sigma > 0$. Then we say that Y has been obtained as a _location-scale transformation_ of X. Here $\mu$ controls how the location is changed and $\sigma$ controls how the scale is changed.

*TODO: How to scale PDF, CDF?*

### Universality
Let F be a CDF which is a continuous function and strictly increasing on the support of the distribution. This ensures that the inverse function $F^{-1}$ exists, as a function from (0,1) to $\mathbb{R}$. We then have the following results.
1. 1. Let $U \sim Unif(0,1)$ and $X = F^{-1}(U)$. Then X is an r.v. with CDF F.
2. 1. Let X be an r.v. with CDF F. Then $F(X) \sim U(0,1)$.
#### Proof
1. $$
   P(X \leq x) = 
   P(F^{-1}(U) \leq x) = 
   P(U \leq F(x)) =
   F(x)
   $$
   because $P(U \leq u) = u$ where $u \in (0,1)$
2. Find CDF of $Y = F(X)$
    $$
   P(Y \leq y) =
   P(F(X) \leq y) = 
   P(X \leq F^{-1}(y)) = 
   F(F^{-1}(y)) = 
   y
   $$
   It follows that $Y \sim U(0, 1)$

