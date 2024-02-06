---
{"dg-publish":true,"permalink":"/world/central-limit-theorem/","created":"","updated":""}
---

#probability 

Under very weak assumptions, the sum of a large number of i.i.d. ([[World/Random variable\|Random variable]]) random variables has an approximately Normal distribution ($\bar{X} \sim N(\mu, \frac{\sigma^{2}}{n})$), regardless of the distribution of the individual r.v.s (as long as mean and variance are finite).

As $n \to \infty$,
$$\sqrt{n}\left(\frac{\bar{X} - \mu}{\sigma}\right) \to N(0,1)$$

**Distribution of the sum**
$$W_{n} = X_{1}+X_{2}+\dots+X_{n} = n\bar{X}$$
$$W_{n} \sim N(n\mu, n\sigma^{2})$$