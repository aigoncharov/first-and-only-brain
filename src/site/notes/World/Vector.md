---
{"dg-publish":true,"permalink":"/world/vector/","created":"","updated":""}
---

#linear_algebra 
## Modulus

$$
x=\begin{bmatrix} a \\ b \\ c \end{bmatrix} = \sqrt[2]{a^2+b^2+c^2}
$$
## Linear combination

$$
cv+dw=c\begin{bmatrix}1 \\ 1\end{bmatrix}+d\begin{bmatrix}2 \\ 3\end{bmatrix}=\begin{bmatrix}c+2d \\ c+3d\end{bmatrix}
$$


System of equations:

$$\begin{cases} 2x -y = 0 \\ -x + 2y = 3 \end{cases}$$

Matrix form:

$$\begin{bmatrix} 2 & -1 \\ -1 & 2 \end{bmatrix} \begin{bmatrix} x  \\ y \end{bmatrix} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}$$
or 
$$Ax = b$$
where $x$ is a *vector*

Linear combination:
$$x \begin{bmatrix} 2 \\ -1 \end{bmatrix} + y \begin{bmatrix} -1 \\ 2 \end{bmatrix} = \begin{bmatrix} 0 \\ 3 \end{bmatrix}$$
Linear combintion of vectors is their **sum**.

## Dot product
$$
\begin{bmatrix}x_1\\x_2\\\dots\\x_n\end{bmatrix}
\cdot
\begin{bmatrix}y_1\\y_2\\\dots\\y_n\end{bmatrix}
=
\sum\limits_{i=1}^n{x_i}{y_i}
$$
or
$$\vec{a}\cdot\vec{b} = |\vec{a}||\vec{b}|cos\theta$$
where $\theta$ is the angle between them

Vectors are **perpendicular** if dot product is 0.

$$\vec{v}\cdot\vec{v} = |\vec{v}|^2$$
For equation $Ax=b$, dot product gives equation of each plane: $row_1\cdot{x}=b_1,\dots,row_n\cdot{x}=b_n$

Then unit vector $\vec{u} = \frac{\vec{v}}{|v|}$

## Cross product
The Cross Product **a × b** of two vectors is **another vector** that is at right angles to both:
![cross_product.png](/img/user/Files/cross_product.png)

$$c = a \times b = |a||b|sin{\theta}\:n$$
where n is a unit vector at the right angles to a and b
![cross_product_value.png](/img/user/Files/cross_product_value.png)

### Formula
$$
c = \begin{bmatrix}a_2b_3-a_3b_2 \\ a_3b_1-a_1b_3 \\ a_1b_2-a_2b_1\end{bmatrix}
$$

### Proof
TODO

## Dependence

$u,v,w$ are independent - no combination except $0u + 0v + 0w = 0$ gives $b=0$
$u,v,w$ are dependent - other combinations like $u + v + w^*$ give $b=0$

## Convolution

Given vectors A(n) and B(m), their convolution is $C(n+m-1) = A*B$, where $C(k) = \sum\limits_{j}A(j)B(k-j+1)$
Result (when n=m):
$$
C(1) = A(1)B(1)
$$
$$
C(2) = A(1)B(2) + A(2)B(1)
$$
$$
C(3) = A(1)B(3) + A(2)B(2) + A(3)B(1)
$$
$$
\dots
$$
$$C(n) = A(1)B(n) + A(2)B(n-1) + \dots + A(n)B(1)$$
$$
\dots
$$
$$
C(2n-1) = A(n)*B(n)
$$
