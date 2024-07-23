---
{"dg-publish":true,"permalink":"/world/squeeze-theorem/"}
---

#math #limits 
*РУ*: Теорема о зажатой последовательности
## Theorem

**For functions:**
Given that $g(x) \leq f(x) \leq h(x)$, $lim_{x \to a}g(x) = L$, $lim_{x \to a} h(x) = L$, then
$$lim_{x \to a} f(x) = L$$

**For series:**
$$a_{n} \leq b_{n} \leq c_{n}, \lim_{n \to \infty} a_{n} = \lim_{n \to \infty} c_{n} = a \rightarrow \exists \lim_{n \to \infty} b_{n} = a $$
Выполняется, даже если последовательность зажата не для всех членов, а только начиная с некоторого номера.
### Application

$$lim_{x \to 0} \frac{sin(x)}{x} = ?$$

![squeeze_theorem.png](/img/user/Files/squeeze_theorem.png)

Areas:
1. Big triangle: $\frac{1tan(x)}{2}$
2. Sector: $\frac{1^2x}{2}$
3. Small triangle: $\frac{1sin(x)}{2}$

$$\frac{1sin(x)}{2} < \frac{1x}{2} < \frac{1tan(x)}{2}$$
$$1 < \frac{x}{sin(x)} < \frac{1}{cos(x)}$$
$$1 > \frac{sin(x)}{x} > cos(x)$$

$$lim_{x \to 0} 1 > lim_{x \to 0} \frac{sin(x)}{x} > lim_{x \to 0} cos(x)$$
$$lim_{x \to 0} cos(x) = 1, lim_{x \to 0} 1 = 1 \rightarrow lim_{x \to 0} \frac{sin(x)}{x} = 1$$