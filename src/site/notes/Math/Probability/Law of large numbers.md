---
{"dg-publish":true,"permalink":"/math/probability/law-of-large-numbers/","created":"","updated":""}
---

#probability 
Let $X_{1}, X_{2}, \dots, X_{n}$ be i.i.d. with finite mean $\mu$ and finite variance $\sigma^{2}$. For all positive integers n, sample mean is
$$
\bar{X} = \frac{\sum\limits_{i=1}^{n}X_{i}}{n}
$$
$$E(\bar{X}) = \mu$$
$$Var(\bar{X}) = \sigma^{2}$$
## Strong
As $n \to \infty$, $\bar{X} \to \mu$ (sample mean converges to true mean).

## Weak
For all $\epsilon > 0$, $P(|X - \epsilon| > 0) \to 0$ as $n \to \infty$ (called convergence in probability).