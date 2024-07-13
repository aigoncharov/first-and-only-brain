---
{"dg-publish":true,"permalink":"/world/derivative/"}
---

#math 

Slope of a tangent line
$$f'(x) = \lim_{h \to 0} \frac{f(x+h) - f(x)}{h}$$
Equation of a tangent line at a point
$$y = f'(x)(x - x_{0}) + y_0$$

Alternative notations:
$$\frac{d}{dx}[f(x)]$$
$$\frac{dy}{dx}$$
## Inverse
$$(f^{-1}(y))'= \frac{1}{f'(x)} =\frac{1}{f'(f^{-1}(y))}$$
Прим. $x = f^{-1}(y)$ по определнию

### Example 1: arcsin
$arcsin(x)' = \frac{1}{sin'(y)} = \frac{1}{cos(y)} = \frac{1}{cos(arcsin(x))} = \frac{1}{\sqrt{1 - sin^{2}(arcsin(x))}} = \frac{1}{\sqrt{1 - x^{2}}}$

## Popular derivatives
$$f'(c) = 0$$
$$f'(x^{n})= nx^{n-1}$$
$$sin'(x) = cos(x)$$
$$cos'(x) = -sin(x)$$
$$tan'(x) = sec^{2}(x) = \frac{1}{cos^{2}(x)} = 1 + tan^{2}(x)$$
$$sec'(x) = sec(x)tan(x)$$
$$csc'(x) = -csc(x)cot(x)$$
$$cot'(x) = -csc^{2}(x)$$
$$ln'(x) = \frac{1}{x}$$
$$log_{a}'(x) = \frac{1}{x \ln(a)}$$
$$(e^{x})'=e^{x}$$
$$(a^{x})' = a^{x} ln(a)$$
## Rules
$$\frac{d}{dx}[cf(x)] = c \frac{d}{dx}[f(x)]$$
$$[f(x) \pm g(x)]' = f'(x) \pm g'(x)$$
$$[f(x)g(x)]'=f'(x)g(x)+f(x)g'(x)$$
$$[\frac{f(x)}{g(x)}]' = \frac{f'(x)g(x)-f(x)g'(x)}{g^2(x)}$$
$$[f(g(x))]' = f'(g(x))g'(x)$$
## Implicit differentiation
Treat y as a function of x. Use chain rule.
$$x^3+y^3=5$$
$$\frac{d}{dx}[x^{3}+y^{3}]=\frac{d}{dx}[5]$$
$$\frac{d}{dx}[x^{3}]+\frac{d}{dx}[y^{3}]=\frac{d}{dx}[5]$$
$$3x^2+3y^2\frac{d}{dx}y=0$$
$$3x^2+3y^2\frac{dy}{dx}=0$$
$$\frac{dy}{dx}=-\frac{3x^2}{3y^2}$$
