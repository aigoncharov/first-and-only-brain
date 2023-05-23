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
2. $lim_{x \to C} f(x)$ exists ([[Math/Calculus/Limits\|Limits]])
3. $lim_{x \to C} f(x) = f(c)$

If $f \circ g$ are continuous at a point C , then:
1. f + g is continuous
2. f - g is continuous
3. $f \cdot g$ is continuous 
4. f / g is continuous unless g(C) = 0

If $f$ has domain $D$ and range $R$ and is continuous, then $f^{-1}$ is continuous on the domain $R$ and the domain $D$ (for inverse functions domain and range swap).

### Intermediate value theorem
If $f$ is continuous on $[a,b]$, some k is between $f(a)$ and $f(b)$, then there is at least one $c$, where $f(c) = k$.

## Increasing, decreasing

1. If $f'(x) > 0$ then f(x) is increasing,
2. If $f'(x) < 0$ then f(x) is decreasing.
3. If $f'(x) = 0$ then f(x) is constant.

Critical number - point where slope is 0 ($f'(x) = 0$ or set the denominator of $f'(x)$ to 0 to catch vertical asymptotes).

First [[Math/Calculus/Derivative\|Derivative]] test:
1. $f'(x) = 0$
2. Find critical numbers. Also numbers that make the derivative undefined - denominator = 0.
3. Put them on a line.
4. Perform sign analysis.

## Concavity
Inflection point - where concavity changes.

1. $f''(x) > 0$ - concave up
2. $f''(x) < 0$ - concave down
3. $f''(x) = 0$ - possible inflection point or constant

Second derivative test:
1. $f''(x) = 0$
2. Put the roots on the line. Also numbers that make the derivative undefined - denominator = 0.
3. Perform sign amalysis.

## Rolle's theorem

If f = 0 at a and b and f is differentiable between a and b, then there must be x such as $f'(x) = 0, x \in (a,b)$

## Mean-value theorem

If f has a secant line between a and b and f is differentiable between a and b, then there must be x such as $f'(x) = \frac{f(b) - f(a)}{b-a}$ (slope of the secant line), where  $x \in (a,b)$