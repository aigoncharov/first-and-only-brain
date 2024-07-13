---
{"dg-publish":true,"permalink":"/world/integral/"}
---

#math  
## Rectangular method (Riemann Sums)
To find an area under a curve from a to b divide $[a,b]$ into n equal sub-sections & create a rectangle in each one.

$$
A = \lim_{n \to \infty} \sum\limits_{i=1}^{i=n} f(x_{i})\Delta x =
\lim_{n \to \infty} \sum\limits_{i=1}^{i=n} f(a + \Delta x \: k)\Delta x
$$

### Example
$$\int_{0}^{x} x^{2} \:dx$$
$$\Delta x = \frac{b-a}{n} = \frac{x - 0}{n} = \frac{x}{n}$$
$$x_{i}= 0 + \frac{ix}{n}$$
$$
\lim_{n \to \infty} \sum\limits_{i=1}^{i=n} f(\frac{ix}{n})\frac{x}{n} = 
\lim_{n \to \infty} \sum\limits_{i=1}^{i=n} (\frac{ix}{n})^{2}\frac{x}{n} =
\lim_{n \to \infty} \frac{1}{n^{3}} \sum\limits_{i=1}^{i=n} i^{2}x^3 =
\lim_{n \to \infty} \frac{x^{3}}{n^{3}} \frac{n(n+1)(2n+1)}{6} =
\lim_{n \to \infty} x^{3} \frac{2n^{2}+3n+1}{6n^{2}} = \frac{x^{3}}{3}
$$

## Antiderivative method
If A(x) is the area under the curve for f(x) on $[a,b]$, then $A'(x) = f(x)$. To find A(x) we "undo" the [[World/Derivative\|Derivative]].

$$\frac{A(x + dx) - A(x)}{dx} = f(x)$$
Thus as $dx \to 0$, $A'(x) = f(x)$
![integral-derivative-relation.png](/img/user/Files/integral-derivative-relation.png)

## Indefinite integral
Given f(x) on some interval I, F - antiderivative, if $F'(x) = f(x)$.

$$\int f(x)\:dx = F(x) + C$$
## Fundamental theorem of calculus
If $f(x)$ is continuous on $[a,b]$, then its area is $A$ such that $A'(x) = f(x)$
$$A(x) = \int_{a}^{x}f(x)\:dx$$
$$A = \int_{a}^{b}f(x)\:dx = F(b) - F(a)$$
**Fundamental theorem of calculus part I:**
$$\frac{d}{dx}\left[\int_{a}^{x}f(x) \:dx\right]= f(x)$$

## Popular integrals

1. $\int n \:dx = nx + C$
2. $\int x^{n}\:dx = \frac{x^{n+1}}{n+1} + C$, $n \neq -1$
3. $\int \frac{1}{x} \:dx = \ln{x} + C$
4. $\int \cos{x} \:dx = \sin{x} + C$
5. $\int \sin{x} \:dx = -\cos{x} + C$
6. $\int \sec^{2}{x} \:dx= \tan{x} + C$
7. $\int \csc^{2}{x} \:dx= -\cot{x} + C$

## Rules

1. $\int c \cdot f(x) \:dx = c \cdot \int f(x) \:dx$
2. $\int f(x) \pm g(x) \:dx = \int f(x) \:dx \pm \int g(x) \:dx$
3. $\int_{a}^{a}f(x)\:dx = 0$
4. $\int_{b}^{a}f(x)\:dx = -\int_{a}^{b}f(x)\:dx$
5. $\int_{a}^{b}f(x)\:dx = \int_{a}^{c}f(x)\:dx + \int_{c}^{b}f(x)\:dx$

## Substitution
1. Pick $u$
	1. Usually "inside of something"
	2. $u'$ must be somewhere else in the integral (disregarding constants)
2. Transform $\int x \:dx$ to $\int u \:du$
3. Do integral
4. Translate back from u to x

### Example
$$\int {(x^{2} + 1)}^{50}2x \:dx$$
$$u=x^{2}+ 1$$
$$\frac{du}{dx} = 2x$$
$$du = 2x \:dx$$
$$dx = \frac{du}{2x}$$
$$
\int {(x^{2} + 1)}^{50}2x \:dx = 
\int {u}^{50} \:du =
\frac{u^{51}}{51} + C =
\frac{(x^{2}+1)^{51}}{51} + C
$$

## Integration by parts

Follows from the product rule for [[World/Derivative\|Derivative]]:
$\int{f(x)g'(x)} = f(x)g(x) - \int{f'(x)g(x)}$

### Example
$\int{x \cos(x) \:dx} = x \sin(x) - \int{\sin(x) \:dx} = x \sin(x) + \cos(x) + C$
## Application
### Volume of solids
$$
V = \lim_{n \to \infty} \sum\limits_{k=1}^{n} A(x_k^{.})\Delta{x}k =
\int_{a}^{b} A(x) \:dx
$$
where $A(x_k^{.})$ is an area of a cross-section

#### Cylindrical shells

$$
V = 2 \Pi \cdot \:average\:radius\:\cdot\:height\:thickness
= \int_{a}^{b} 2\Pi x f(x) dx
$$
![volume_cylindrical_shell.png](/img/user/Files/volume_cylindrical_shell.png)

### Length of a curve
$$
L = \lim_{n \to \infty} \sum\limits_{k=1}^{n} \sqrt{1 + (f'(x_{k^{.}}))^{2}}\: \Delta x
= \int_{a}^{b} \sqrt{1 + (f'(x_{k^{.}}))^{2}} \:dx
$$

### Area of a a surface
Circumference x length
$$S.A. = \int_{a}^{b} 2 \Pi f(x) \sqrt{1 + (f'(x))^{2}} \:dx $$
