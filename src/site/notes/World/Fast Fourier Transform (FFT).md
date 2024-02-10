---
{"dg-publish":true,"permalink":"/world/fast-fourier-transform-fft/","created":"","updated":""}
---

#math #divide_and_conquer #polynomials 
## Premise
Given $A(x) = a_{0} + a_{1}x + a_{2}x^{2} + \dots + a_{n-1}x^{n-1}$ and $B(x) = b_{0} + b_{1}x + b_{2}x^{2} + \dots + b_{n-1}x^{n-1}$, compute $C(x) = A(x)B(x) = c_{0} + c_{1}x + c_{2}x^{2} + \dots + c_{2n-2}x^{2n-2}$, where $c_{i} = a_{0}b_{i} + a_{1}b_{i-1} + \dots + a_{i}b_{0}$.
In other words, given vectors ([[World/Vector\|Vector]]) $a = \begin{bmatrix} a_{0} \\ \dots \\ a_{i} \end{bmatrix}$ and $b = \begin{bmatrix} b_{0} \\ \dots \\ b_{i} \end{bmatrix}$, compute $c=a*b$ - convolution.

$$
C(0) = A(0)B(0)
$$
$$
C(1) = A(0)B(1) + A(1)B(0)
$$
$$
C(2) = A(0)B(2) + A(1)B(1) + A(3)B(0)
$$
$$
\dots
$$
$$C(n-1) = A(0)B(n-1) + A(1)B(n-2) + \dots + A(n-1)B(0)$$
$$
\dots
$$
$$
C(2n-2) = A(n-1)*B(n-1)
$$
## Recurrence
Polynomial can be represented by its coefficients and by its values (points). FFT converts from one to another.

Polynomial A(x) with deg (n-1) is uniquely determined by n distinct points. So `C(2n) = A(2n)*B(2n)`. 

We choose the points in a way that: $A(x_{n+i}) = A(-x_{i})$ (plus-minus property). This way: even terms are the same (even power), odd terms are the opposite.

Split A(x) into two polynomials:
$$
A_{even}(y) = a_{0}+a_{2}y + a_{4}y^{2} + \dots + a_{n-2}y^{\frac{n-2}{2}}
$$
$$
A_{odd}(y) = a_{1}+a_{3}y + a_{4}y^{2} + \dots + a_{n-1}y^{\frac{n-2}{2}}
$$
$$A(x) = A_{even}(x^{2}) + x A_{odd}(x^{2})$$
Because of plus-minus property: $A(x_{i}) = A_{even}(x^{2}) + x_{i} A_{odd}(x^{2})$ and $A(x_{n+i}) = A(-x_{i}) = A_{even}(x^{2}) - x_{i} A_{odd}(x^{2})$
-> we can evaluate (expensive operation) A_even and A_odd only at n points and then calculate A at 2n points using the results for A_even and A_odd.

**Runtime**: $T(n) = 2T\left(\frac{n}{2}\right) + O(n) = n log(n)$

Next problem: satisfy plus-minus property on each level of recursion. 
On top level: $x_{n+i} = -x_{i}$
On next level: $x_{\frac{n}{2}+i}^{2}=-x_{i}^{2}$
Solution: [[World/Complex numbers\|Complex numbers]]

## Roots of unity
$w_{i} = (1, \frac{2\pi}{i})$
$w_{i}^{2} = w_{i/2}$, for example, $w_{16}^{2}=w_{8}$

![roots_of_unity_1.png](/img/user/Files/roots_of_unity_1.png)
![roots_of_unity_2.png](/img/user/Files/roots_of_unity_2.png)

## Pseudocode

```
FFT(a,w):
	if n=1, return A(1)
	define a_even (a_0...a_n-2) and a_odd(a_1...a_n-1)
	
	call FFT(a_even, w^2): get A_even(w^0)...A_even(w^n-2)
	call FFT(a_odd, w^2): get A_odd(w^0)...A_odd(w^n-2)

	for j=0->n/2-1: 
		A(w^j) = A_even(w^2j) + w^j A_odd(w^2j)
		A(w^n/2+j) = A_even(w^2j) - w^j A_odd(w^2j)

	return (A(w^0)...A(w^n-1))
```
## Inverse FFT

From linear algebra point of view, FFT computes $A = M_{n}(w_{n})a$, where $M_{n}(w_{n})$ is a matrix of roots of unity
$$
\begin{bmatrix} A(1) \\  A(w_{n}) \\ \dots \\ A(w_{n}^{n-1}) \end{bmatrix} = 
\begin{bmatrix} 
1 & 1 & 1 & \dots & 1 \\
1 & w_{n} & w_{n}^{2} & \dots & w_{n}^{n-1} \\
1 & w_{n}^{2} & w_{n}^{4} & \dots & w_{n}^{2(n-1)} \\
\dots \\
1 & w_{n}^{n-1} & w_{2(n-1)} & \dots & w_{n}^{(n-1)(n-1)} \\
\end{bmatrix}
\begin{bmatrix} a_{0} \\  a_{1} \\ \dots \\ a_{n} \end{bmatrix}
$$
If we could compute the inverse of $M_{n}(w_{n})$, then we could compute the coefficients of the polynomial from the its evaluated points:  $a = M^{-1}_{n}(w_{n})A$

**Lemma:**
$$
M^{-1}_{n}(w_{n}) = \frac{1}{n}M_{n}(w_{n}^{-1})
$$

$$
w_{n}^{-1} w_{n} = 1 \to w_{n}^{-1} = w_{n}^{n-1}
$$

## Polynomial multiplication
1. Run FFT for 2n roots of unity for polynomial A. Get back points A_res.
1. Run FFT for 2n roots of unity for polynomial B. Get back points B_res.
2. Multiply A_res and B_res. Get points for polynomial C.
3. Run inverse FFT