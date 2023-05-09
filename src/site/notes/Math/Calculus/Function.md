---
{"dg-publish":true,"permalink":"/math/calculus/function/","created":"","updated":""}
---

#calculus  

Each input X has *exactly* one output.

**Domain** - set of input values
**Range** - set of output values

Even function: $f(-x)=f(x)$, symmetric about the y-axis
Odd function: $f(-x)=-f(x)$, symmetric about the origin

**Polynomial** is an expression consisting of indeterminates (also called variables) and coefficients, that involves only the operations of addition, subtraction, multiplication, and positive-integer powers of variables.

## Combination

$$(f+g)(x)=f(x)+g(x)$$
$$(f-g)(x)=f(x)-g(x)$$
$$(f \times g)(x)=f(x)g(x)$$
$$(\frac{f}{g})(x)=\frac{f(x)}{g(x)}$$
where $g(x) \neq 0$

## Composition
$$f(x) = x^{3}- 4$$
$$g(x)=\sqrt{x}$$
$$(f\circ{g})(x)=f(g(x)) = f(\sqrt{x}) = (\sqrt{x})^{3}- 4$$
$$(g\circ{f})(x) = \sqrt{x^{3}- 4}$$


## Continuity

f is continuous at a point C if:
1. f(c) is defined
2. $lim_{x \to C} f(x)$ exists
3. $lim_{x \to C} f(x) = f(c)$

If $f \circ g$ are continuous at a point C , then:
1. f + g is continuous
2. f - g is continuous
3. $f \cdot g$ is continuous 
4. f \ g is continuous unless g(C) = 0

If $f$ has domain $D$ and range $R$ and is continuous, then $f^{-1}$ is continuous on the domain $R$ and the domain $D$ (for inverse functions domain and range swap).

### Intermediate value theorem
If $f$ is continuous on $[a,b]$, some k is between $f(a)$ and $f(b)$, then there is at least one $c$, where $f(c) = k$.