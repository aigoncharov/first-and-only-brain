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

Runtime: $T(n) = 2T\left(\frac{n}{2}\right) + O(n) = n log(n)$

Next problem: satisfy plus-minus property on each level of recursion. 
On top level: $x_{n+i} = -x_{i}$
On next level: $x_{\frac{n}{2}+i}^{2}=-x_{i}^{2}$
Solution: [[World/Complex numbers\|Complex numbers]]

## Roots of unity
$w_{i} = (1, \frac{2\pi}{i})$
$w_{i}^{2} = w_{i/2}$, for example, $w_{16}^{2}=w_{8}$

![roots_of_unity_1.png](/img/user/Files/roots_of_unity_1.png)
![roots_of_unity_2.png](/img/user/Files/roots_of_unity_2.png)

