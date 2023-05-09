---
{"dg-publish":true,"permalink":"/math/calculus/limits/","created":"","updated":""}
---

#calculus 

$\lim_{x \to a} f(x)$ exists if $lim_{x \to a^{+}} f(x) = lim_{x \to a^{-}}f(x)$

## Basics
$$lim_{x \to a} C = C$$
$$lim_{x \to a} x = a$$
$$lim_{x \to 0^{-} \frac{1}{x}}= -\infty$$
$$lim_{x \to 0^{+} \frac{1}{x}}= +\infty$$
## Properties
Gien that:
$$lim_{x \to a} f(x) = L_1$$
$$lim_{x \to a} g(x) = L_2$$
Properties:
1. $$lim_{x \to a} [f(x) \pm g(x)] = lim_{x \to a} f(x) \pm lim_{x \to a} g(x)$$
2. $$lim_{x \to a} [f(x) \times g(x)] = lim_{x \to a} f(x) \times lim_{x \to a} g(x)$$
3. $$lim_{x \to a} [\frac{f(x)}{g(x)}] = \frac{lim_{x \to a} f(x)}{lim_{x \to a} g(x)}$$
   where $lim_{x \to a} g(x) \neq 0$
4. $$lim_{x \to a} [f(x)]^n = [lim_{x \to a} f(x)]^n$$
5. $$lim_{x \to a} P(x) = P(a)$$
   where P(x) is a polynomial ([[Math/Calculus/Function\|Function]])
6. $$lim_{x \to a} f\circ{g}(x) = f(lim_{x \to a} g(x)) $$
   if f(x) is continuous

## Squeeze theorem

Given that $g(x) \leq f(x) \leq h(x)$, $lim_{x \to a}g(x) = L$, $lim_{x \to a} h(x) = L$, then
$$lim_{x \to a} f(x) = L$$
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
