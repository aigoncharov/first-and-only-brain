---
{"dg-publish":true,"permalink":"/math/probability/averages/","created":"","updated":""}
---

#probability 

## Expected value (mean)
### Discrete
$$E(X) = \sum\limits_{j = 1}^{\infty} x_{j} P(X = x_{j})$$
### Linearity of expectation
$$E(X + Y) = E(X) + E(Y)$$
$$E(cX) = cE(x)$$
**Holds for dependent RVs!**

## Law of the unconscious statistician (LOTUS)
If X is a discrete r.v. and g(x) is a function $\mathbb{R} \to \mathbb{R}$, then
$$E(g(X)) = \sum\limits_{x}g(x)P(X = x)$$
where the sum is taken for all possible values of X.

## Variance and standard deviation
Variance: $Var(X) = E(X - E(X))^{2} = E(X^{2}) - (E(X))^{2}$
Standard deviation: $SD(X) = \sqrt{Var(X)}$

### Properties
1. $Var(X + c) = Var(X)$ for any constant $c$
2. $Var(cX) = c^{2}Var(X)$
3. If X and Y are independent, then $Var(X + Y) = Var(X) + Var(Y)$
4. The only R.V.s to have 0 variance are constants. For others, $Var(X) > 0$.
