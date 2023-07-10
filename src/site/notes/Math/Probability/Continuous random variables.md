---
{"dg-publish":true,"permalink":"/math/probability/continuous-random-variables/","created":"","updated":""}
---

#probability 
An r.v. has a _continuous distribution_ if its CDF is differentiable. We also allow there to be endpoints (or finitely many points) where the CDF is continuous but not differentiable, as long as the CDF is differentiable everywhere else. A _continuous random variable_ is a random variable with a continuous distribution.

## Probability density function (PDF)
For a continuous r.v. X with CDF F, the _probability density function_ (PDF) of X is the derivative $f$ of the CDF, given by $f(x) = F'(x)$. The _support_ of X, and of its distribution, is the set of all x where f(x) > 0.

### PDF -> CDF
$$F(x) = \int_{-\infty}^{x} f(t) \:dt$$
### Validity
1. Nonnegative. $f(x) \geq 0$
2. Integrates to 1: $\int_{-\infty}^{\infty} f(x) = 1$

## Expected value (mean)
$$E(X) = \int_{-\infty}^{\infty}xf(x)dx$$
It the support of X is not $(-\infty, \infty)$, then we can integrate over the support only.

### Linearity of expectation
See [[Math/Probability/Discrete random variables\|Discrete random variables]]

## Law of the unconscious statistician (LOTUS)
If X is a continuous r.v. and g(x) is a function $\mathbb{R} \to \mathbb{R}$, then
$$E(g(X)) = \int_{-\infty}^{\infty}g(x)f(x)$$
where the sum is taken for all possible values of X.